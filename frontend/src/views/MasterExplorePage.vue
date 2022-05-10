<template>
  <div class="container mt-6" style="background-color: rgb(115, 187, 169)">
    <nav class="navbar" role="navigation" aria-label="main navigation">
      <div class="navbar-brand">
        <a
          class="navbar-item"
          href="https://new.reg.kmitl.ac.th/admission/#/master/explore"
        >
          <img
            src="https://new.reg.kmitl.ac.th/admission/kmitl_logo.png"
            alt="Bulma: Free, open source, and modern CSS framework based on Flexbox"
            width="112"
            height="28"
          />
        </a>

        <a
          role="button"
          class="navbar-burger"
          aria-label="menu"
          aria-expanded="false"
        >
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
        </a>
      </div>
    </nav>
    <div class="columns is-centered">
      <div class="column is-centered has-text-centered has-text-white">
        <h1>ค้นหาหลักสูตรที่เปิด</h1>
      </div>
    </div>
    <div class="columns">
      <div class="column">
        <v-autocomplete
          v-model="facultylist"
          :items="faculty"
          dense
          chips
          small-chips
          label="ค้นหา 'คณะ'"
          multiple
          solo
        ></v-autocomplete>
      </div>
      <div class="column">
        <v-autocomplete
          v-model="roundlist"
          :items="round"
          dense
          chips
          small-chips
          label="ค้นหา 'รอบรับสมัคร'"
          multiple
          solo
        ></v-autocomplete>
      </div>
      <div class="column">
        <v-autocomplete
          v-model="programlist"
          :items="program"
          dense
          chips
          small-chips
          label="ค้นหา 'โครงการ'"
          multiple
          solo
        ></v-autocomplete>
      </div>
    </div>
    <div class="columns">
      <div class="column is-one-third">
        <v-autocomplete
          v-model="syllabuslist"
          :items="syllabus"
          dense
          chips
          small-chips
          label="ค้นหาหลักสูตร ไทย / นานาชาติ"
          multiple
          solo
        ></v-autocomplete>
      </div>
    </div>
    <div class="columns">
      <div class="column">
        <v-autocomplete
          v-model="announcementlist"
          :items="announcement"
          dense
          chips
          small-chips
          label="คำค้นหาเพิ่มเติม (Enter เพื่อแยกคำ) [ระบบจะค้นจากชื่อคณะ,หลักสูตร]"
          multiple
          solo
        ></v-autocomplete>
      </div>
    </div>
    <div class="columns">
      <div class="column">
        <div class="card">
          <header class="card-header">
            <p class="card-header-title">
              หลักสูตร : การวางแผนชุมชนเมืองและสภาพแวดล้อม
            </p>
            <button class="card-header-icon" aria-label="more options">
              <span class="icon">
                <i class="fas fa-angle-down" aria-hidden="true"></i>
              </span>
            </button>
          </header>
          <div class="card-content">
            <div class="content">
              หลักสูตร : การวางแผนชุมชนเมืองและสภาพแวดล้อม
              <br />
              คณะ : สถาปัตยกรรม ศิลปะและการออกแบบ
              <br />
              วันที่เปิดรับสมัคร :
              <time datetime=""> 24 กุมภาพันธ์ 2022 - 31 พฤษภาคม 2022</time>
            </div>
          </div>
          <footer class="card-footer">
            <a href="#" class="card-footer-item">สมัคร</a>
            <a href="#" class="card-footer-item">ประกาศรับสมัคร</a>
            <a href="#" class="card-footer-item">คุณสมบัติผู้สมัคร</a>
          </footer>
        </div>
      </div>
    </div>
    <div class="columns">
      <div class="column">
        <div class="card">
          <header class="card-header">
            <p class="card-header-title">
              หลักสูตร : การวางแผนชุมชนเมืองและสภาพแวดล้อม
            </p>
            <button class="card-header-icon" aria-label="more options">
              <span class="icon">
                <i class="fas fa-angle-down" aria-hidden="true"></i>
              </span>
            </button>
          </header>
          <div class="card-content">
            <div class="content">
              หลักสูตร : การวางแผนชุมชนเมืองและสภาพแวดล้อม
              <br />
              คณะ : สถาปัตยกรรม ศิลปะและการออกแบบ
              <br />
              วันที่เปิดรับสมัคร :
              <time datetime=""> 24 กุมภาพันธ์ 2022 - 31 พฤษภาคม 2022</time>
            </div>
          </div>
          <footer class="card-footer">
            <a href="#" class="card-footer-item">สมัคร</a>
            <a href="#" class="card-footer-item">ประกาศรับสมัคร</a>
            <a href="#" class="card-footer-item">คุณสมบัติผู้สมัคร</a>
          </footer>
        </div>
      </div>
    </div>
    <div class="columns">
      <div class="column">
        <div class="card">
          <header class="card-header">
            <p class="card-header-title">
              หลักสูตร : การวางแผนชุมชนเมืองและสภาพแวดล้อม
            </p>
            <button class="card-header-icon" aria-label="more options">
              <span class="icon">
                <i class="fas fa-angle-down" aria-hidden="true"></i>
              </span>
            </button>
          </header>
          <div class="card-content">
            <div class="content">
              หลักสูตร : การวางแผนชุมชนเมืองและสภาพแวดล้อม
              <br />
              คณะ : สถาปัตยกรรม ศิลปะและการออกแบบ
              <br />
              วันที่เปิดรับสมัคร :
              <time datetime=""> 24 กุมภาพันธ์ 2022 - 31 พฤษภาคม 2022</time>
            </div>
          </div>
          <footer class="card-footer">
            <a href="#" class="card-footer-item">สมัคร</a>
            <a href="#" class="card-footer-item">ประกาศรับสมัคร</a>
            <a href="#" class="card-footer-item">คุณสมบัติผู้สมัคร</a>
          </footer>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "../plugins/axios";
export default {
  data() {
    return {
      faculty: ["วิทยาศาสตร์", "แพทย์ศาสตร์", "เทคโนโลยีสารสนเทศ"],
      round: [
        "( 1/2565 ) รอบ 1 - รับสมัครประจำภาคการศึกษา",
        "( 1/2565 ) รอบ 1 - รับสมัครประจำภาคการศึกษา",
        "( 2/2565 ) รอบ 1 - รับสมัครประจำภาคการศึกษา",
      ],
      program: [
        "รับเข้า 1/2565 คณะวิทยาศาสตร์",
        "รับเข้า 1/2565 คณะแพทย์ศาสตร์",
        "รับเข้า 1/2565 คณะเทคโนโลยีสารสนเทศ",
      ],
      syllabus: ["หลักสูตรนานาชาติ", "หลักสูตรไทย"],
      announcement: [],
      announcementlist: null,
      facultylist: null,
      roundlist: null,
      programlist: null,
      syllabuslist: null,
    };
  },
  methods: {},
  created() {
    axios
      .get("/rooms")
      .then((response) => {
        console.log(response.data);
        this.rooms = response.data;
      })
      .catch((err) => {
        console.log(err.response.data);
      });
  },
};
</script>
