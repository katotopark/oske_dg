<template>
  <el-container>
    <el-main>
      <!-- <div
        v-if="!open"
        class="confirm-box">
        <el-button
          class="confirm-button"
          @click="open = true">
          hello
        </el-button>
      </div> -->
      <el-row
        class="contain"
        type="flex"
        justify="center">
        <el-col
          :xs="22"
          :sm="20"
          :md="20">
          <el-row>
            <h2 class="title">
              İyi ki doğdun {{ hitap }}
              <el-button
                class="name-button"
                @click="handleClick">
                {{ currentName }}.
              </el-button>
            </h2>
          </el-row>
          <el-row>
            <el-button
              class="mode-button"
              @click="changeMode">Mod: <span>{{ currentMode }}</span></el-button>
          </el-row>
        </el-col>
      </el-row>
    </el-main>
    <el-footer>
      {{ footerString }}
    </el-footer>
  </el-container>

</template>

<script>
export default {
  data() {
    return {
      namesArr: [
        'Özge',
        'sis',
        'lil sis',
        'minnoş',
        'yavru',
        'küçük ö',
        'ö',
        'kardeşim',
        'kardeş',
        'aftika',
        'ganve',
        'tontiriks',
        'tonti',
        'baby mama',
        '2'
      ],
      footerString: `Ö'den <3'lerle - 6.1.19`,
      currentName: '',
      currentMode: '',
      modes: ['Normal', 'Kibariye', 'Öküzbaş'],
      modeCounter: 0,
      buttonText: '',
      hitap: '',
      open: false
    }
  },
  watch: {
    currentMode() {
      if (this.currentMode == this.modes[0]) this.hitap = ''
      else if (this.currentMode == this.modes[1]) this.hitap = 'sayın'
      else if (this.currentMode == this.modes[2]) this.hitap = 'lan'
    }
  },
  created() {
    this.currentName = 'Özge'
    this.currentMode = this.modes[this.modeCounter]
    this.hitap = ''
  },
  methods: {
    handleClick() {
      this.getNewName()
    },
    getNewName() {
      let random = Math.floor(Math.random() * this.namesArr.length)
      this.currentName = this.namesArr[random]
    },
    changeMode() {
      if (this.modeCounter < this.modes.length - 1) {
        this.modeCounter++
      } else {
        this.modeCounter = 0
      }
      this.currentMode = this.modes[this.modeCounter]
    }
  }
}
</script>

<style>
div.confirm-box {
  min=width: 100vh;
  min-height: 100vh;
  background-color: #82c2a2;
}
.el-button.confirm-button {
  background-color: inherit;
  border-radius: 0px;
  color: #b75556;
  font-size: 3rem;
  font-family: inherit;
  font-weight: 300;
  padding: 20px 15px;
  border: 4px solid #b75556;
}
.contain {
  background-color: #82c2a2;
  min-height: 100vh;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.title {
  display: block;
  font-weight: 500;
  font-size: 70px;
  color: #b75556;
  letter-spacing: 1px;
  line-height: 120px;
  margin-bottom: 20px;
}
.el-button.name-button,
.el-button.name-button:active,
.el-button.name-button:visited,
.el-button.name-button:focus {
  font-family: inherit;
  font-size: inherit;
  font-weight: inherit;
  border-radius: 0px;
  color: #b75556;
  background-color: #82c2a2;
  border: 4px solid #b75556;
  padding: 20px 15px;
}
.el-button.name-button:hover {
  color: #82c2a2;
  background-color: #b75556;
}

.el-button.mode-button {
  background-color: inherit;
  border-radius: 0px;
  color: #b75556;
  font-size: 3rem;
  font-family: inherit;
  font-weight: 300;
  padding: 20px 15px;
  margin-top: 60px;
  margin-bottom: 30px;
  border: 4px solid #b75556;
}
.el-button.mode-button:hover,
.el-button.mode-button:active {
  color: #82c2a2;
  background-color: #b75556;
}
.el-main {
  padding: 0px;
}
.el-footer {
  background-color: #b75556;
  color: #82c2a2;
  text-align: center;
  justify-content: center;
  font-size: 1rem;
  height: 25px !important;
}
</style>
