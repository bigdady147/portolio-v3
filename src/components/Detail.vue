<script setup>
import { ref, defineProps, watch } from "vue";
const props = defineProps({
  section: {
    type: String,
    default: "stack",
  },
});
const section_selected = ref(props.section);
watch(
  () => props.section,
  (newValue, oldValue) => {
    if (newValue !== oldValue) {
      section_selected.value = newValue;
    }
  },
  { deep: true }
);
</script>

<template>
  <div v-if="section_selected === 'home'" class="detail">
    <div class="detail-home">
      <div class="heading-detail">
        <h2>ABOUT ME</h2>
        <div class="line"></div>
      </div>
      <div class="main-detail">
        <small>
          Hello! I am Nguyen Truong An, and I am thrilled to welcome you to my
          portfolio. <br />
          As a passionate and versatile full-stack developer, I have a keen
          interest in exploring the latest cutting-edge technologies.<br />
          My journey in the field of web development has been truly
          exhilarating, and I constantly strive to enhance my skills and embrace
          emerging trends in the industry.<br />
          I believe that creativity and innovation are key to creating
          high-quality products that deliver real value to users.
        </small>
      </div>
      <hr />
      <div class="heading-detail">
        <h2>Objectives</h2>
        <div class="line"></div>
      </div>
      <div class="main-detail">
        <small>
          Constantly learning and developing myself, leveraging my existing
          skills gained from years of work to strive to become a passionate
          software engineer. <br />
          Delivering complete applications and products to customers,
          contributing to the company. <br />
          Develop advanced coding skills, analyze customer business
          requirements, design project architecture, build complete systems and
          infrastructure, and deploy application models from the development
          environment to the production environment
        </small>
        <small> </small>
      </div>

      <hr />
      <div class="heading-detail">
        <h2>WHAT I DO !</h2>
        <div class="line"></div>
      </div>
      <div class="more-detail mt-2">
        <div class="more-detail-main">
          <div class="heading d-flex align-items-center">
            <div class="icon icon-vue">
              <i class="fa-brands fa-vuejs"></i>
            </div>
            <small class="text">FRONT-END</small>
          </div>
          <div class="desc">
            As a developer, I find myself most captivated by the power and
            flexibility of VueJS. I'm always eager to dive into new projects
            that leverage VueJS and discover innovative ways to create fast,
            scalable, and user-friendly applications.
          </div>
        </div>
        <div class="more-detail-main mt-lg-2">
          <div class="heading d-flex align-items-center">
            <div class="icon text-danger">
              <i class="fa-brands fa-laravel"></i>
            </div>
            <small class="text">BACK-END</small>
          </div>
          <div class="desc">
            I have the ability to develop and build data structures based on
            analyzing business requirements. I am particularly fascinated by the
            process of developing APIs and server-side processing functions,
            with the goal of enhancing application performance quickly and
            efficiently
          </div>
        </div>
      </div>
    </div>
  </div>
  <div v-if="section_selected === 'stack'" class="stack">
    <div class="stack-home">
      <div class="heading-detail">
        <h2>TECH STACK</h2>
        <div class="line"></div>
      </div>
      <hr />
      <div class="heading-detail">
        <h2>Front-end Development</h2>
        <div class="line"></div>
      </div>
      <div class="list-skill">
        <div class="skill-container">
          <div class="icon">
            <i style="color: orange" class="fa-brands fa-html5"></i>
          </div>
          <div class="name">HTML</div>
        </div>
        <div class="skill-container">
          <div class="icon">
            <i class="fa-brands fa-css3-alt text-primary"></i>
          </div>
          <div class="name">CSS</div>
        </div>
        <div class="skill-container">
          <div class="icon">
            <i style="color: #e23a8e" class="fa-brands fa-sass"></i>
          </div>
          <div class="name">Sass</div>
        </div>
        <div class="skill-container">
          <div class="icon">
            <i class="fa-brands fa-js text-warning"></i>
          </div>
          <div class="name">Javascript</div>
        </div>
        <div class="skill-container">
          <div class="icon">
            <i class="fa-brands fa-vuejs text-success"></i>
          </div>
          <div class="name">Vue2 & Vue3</div>
        </div>
        <div class="skill-container">
          <div class="icon">
            <i style="color: #9c2bc9" class="fa-brands fa-bootstrap"></i>
          </div>
          <div class="name">Bootstrap</div>
        </div>
        <div class="skill-container">
          <div class="images">
            <img src="/images/jquery.png" alt="" />
          </div>
          <div class="name">jQuery</div>
        </div>
        <div class="skill-container">
          <div class="images">
            <img src="/images/chartjs.png" alt="" />
          </div>
          <div class="name">ChartJs</div>
        </div>
        <div class="skill-container">
          <div class="images">
            <img src="/images/excel.png" alt="" />
          </div>
          <div class="name">ExcelJS</div>
        </div>
        <div class="skill-container">
          <div class="icon">
            <i class="fa-solid fa-video text-danger"></i>
          </div>
          <div class="name">RecordRTC</div>
        </div>
        <div class="skill-container">
          <div class="icon">
            <i class="fa-brands fa-js text-warning"></i>
          </div>
          <div class="name">Javascript libraries</div>
        </div>
        <div class="skill-container">
          <div class="icon">
            <i class="fa-solid fa-globe text-primary"></i>
          </div>
          <div class="name">Open API</div>
        </div>
      </div>
      <hr />
      <div class="heading-detail">
        <h2>Back-end Development</h2>
        <div class="line"></div>
      </div>
      <div class="list-skill">
        <div class="skill-container">
          <div class="icon">
            <i style="color: #5025c4" class="fa-brands fa-php"></i>
          </div>
          <div class="name">PHP</div>
        </div>
        <div class="skill-container">
          <div class="icon">
            <i class="fa-brands fa-laravel text-danger"></i>
          </div>
          <div class="name">Laravel</div>
        </div>
        <div class="skill-container">
          <div class="images">
            <img src="/images/sql.png" alt="" />
          </div>
          <div class="name">MySQL</div>
        </div>
        <div class="skill-container">
          <div class="images">
            <img src="/images/mongodb.png" alt="" />
          </div>
          <div class="name">MongoDB</div>
        </div>
        <!-- <div class="skill-container">
          <div class="icon">
            <i style="color: #e23a8e" class="fa-brands fa-sass "></i>
          </div>
          <div class="name">Sass</div>
        </div> -->
      </div>
      <hr />
      <div class="heading-detail">
        <h2>Others</h2>
        <div class="line"></div>
      </div>
      <div class="list-skill">
        <div class="skill-container">
          <div class="icon">
            <i class="fa-brands fa-github"></i>
          </div>
          <div class="name">Github</div>
        </div>
        <div class="skill-container">
          <div class="icon">
            <i style="color: orange" class="fa-brands fa-gitlab"></i>
          </div>
          <div class="name">Gitlab</div>
        </div>
      </div>
    </div>
  </div>

  <div v-if="section_selected === 'exp'" class="exp">
    <div class="exp-home">
      <div class="heading-detail">
        <h2>Experience</h2>
        <div class="line"></div>
      </div>
    </div>
    <div class="exp-container">
      <div class="line"></div>

      <div class="card-exp">
        <div class="dot"></div>
        <div class="content">
          <div class="heading">
            <span class="name">Jobtest</span>
            <span class="time">Jul 2022 - Present</span>
          </div>
          <div class="desc">
            <div class="section-data">
              <div
                class="project d-flex justify-content-between align-items-center"
              >
                <span style="font-weight: 600">Platform: Jobtest.vn</span>
                <!-- <span>Jul 2022 - Aug 2023</span> -->
              </div>
              <div class="title">Front-end Engineer</div>
              <div class="about">
                JobTest provides competency assessment solutions for businesses
                and individuals - helping companies and workers understand their
                abilities to "optimize" resources and maximize performance.
              </div>
            </div>
            <div class="todo">
              <span>WEB:</span>
              <br />
              <ul class="mb-0">
                <li>Create layout looks like a designer's design on Figma.</li>
                <li>Apply REST API to get data and binding data.</li>
                <li>Writing reusable components - system design.</li>
                <li>
                  Build candidate assessment pages with multiple-choice
                  questions, essays, and answers recorded directly through
                  question prompts, etc.
                </li>
                <li>
                  Analyze the customer specification documents, and create
                  charts to represent the candidate requirements specifications
                  after the assessment.
                </li>
              </ul>
              <span>Admin:</span>
              <ul>
                <li>
                  Calculate and process the parameters for the report, draw
                  charts,...
                </li>
                <li>CRUD of statistical lists</li>
              </ul>
            </div>
          </div>
          <div class="desc">
            <div class="section-data">
              <div
                class="project d-flex justify-content-between align-items-center"
              >
                <span style="font-weight: 600">Web Application: AiHR</span>
                <!-- <span>Jul 2022 - Aug 2023</span> -->
              </div>
              <div class="title">Front-end Engineer</div>
              <div class="about">
                The AiHR human resource software is a human resource management
                platform, typically designed to assist businesses in managing
                employee information, recruitment processes, training,
                performance evaluation, and other activities related to human
                resources. AiHR can provide tools to automate HR management
                tasks, improve internal communication, and optimize workflows.
              </div>
            </div>
            <div class="todo">
              <span>Front-end:</span>
              <br />
              <ul class="mb-0">
                <li>
                  Develop a KPI and productivity assessment system for companies
                  specializing in large-scale assembly line production.
                </li>
                <li>Upgrade the project from Vue2 to Vue3.</li>
                <li>Apply REST API to get data and binding data.</li>
                <li>Writing reusable components - system design.</li>
              </ul>
              <span>Back-end:</span>
              <ul>
                <li>
                  Develop a database for the project based on the structure
                  (Laravel).
                </li>
                <li>
                  Build APIs related to the WPI productivity assessment system
                  from product allocation and output, and create formulas to
                  calculate work efficiency for applying to salary bonuses P2
                  and P3.
                </li>
                <li>Build APIs for third parties to connect.</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
      <div class="card-exp mt-3">
        <div class="dot"></div>
        <div class="content">
          <div class="heading">
            <span class="name">Pix Interaction</span>
            <span class="time">May 2022 - Jun 2022</span>
          </div>
          <div class="desc">
            <div class="section-data">
              <div
                class="project d-flex justify-content-between align-items-center"
              >
                <span style="font-weight: 600">Platform: Jobtest.vn</span>
                <!-- <span>Jul 2022 - Aug 2023</span> -->
              </div>
              <div class="title">Intern</div>
              <div class="about">
                Pix Interaction is a company specializing in IT solutions,
                focusing on software development and user experience (UX/UI)
                design. With a team of experienced professionals, the company is
                committed to delivering high-quality products and services to
                optimize workflow for its clients.
              </div>
            </div>
            <div class="todo">
              <span>WEB:</span>
              <br />
              <ul class="mb-0">
                <li>Create layout looks like a designer's design on Figma.</li>
                <li>Apply REST API to get data and binding data.</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div v-if="section_selected === 'education'" class="education">
    <div class="education-home">
      <div class="heading-detail">
        <h2>EDUCATION & ACHIEVEMENTS</h2>
        <div class="line"></div>
      </div>
      <div class="edu-card">
        <div class="heading d-flex justify-content-between align-items-center">
          <span class="name">Thu Duc Technology College</span>
          <span class="time">Aug 2020 - May 2022</span>
        </div>
        <div class="desc">
          <small>Major: Information Technology</small>
        </div>
      </div>
      <div class="edu-card mt-2">
        <div class="heading d-flex justify-content-between align-items-center">
          <span class="name">English</span>
        </div>
        <div class="desc">
          <small>Toeic: 550 point</small>
        </div>
      </div>
      <div class="edu-card mt-2">
        <div class="heading d-flex justify-content-between align-items-center">
          <span class="name">Jobtest</span>
          <span class="time">Quater III - 2023</span>
        </div>
        <div class="desc">
          <small>The dedicated employee</small>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.detail {
  padding: 20px;
  background: #fff;
  &-home {
    .heading-detail {
      display: flex;
      align-items: center;
      gap: 10px;
      h2 {
        font-size: 16px;
        line-height: 22px;
        font-weight: 600;
      }
      .line {
        width: 10%;
        height: 2px;
        background: #ff512f;
      }
    }
    .more-detail {
      display: flex;
      justify-content: space-between;
      @media screen and (max-width: 992px) {
        flex-direction: column;
        .mt-lg-2{
          margin-top: 20px;
        }
      }
      &-main {
        max-width: 48%;
        background-color: #f2f7fc;
        border-radius: 6px;
        padding: 12px 20px;
        transition: all 0.2s linear;
        @media screen and (max-width: 992px) {
          max-width: 100%;

        }
        &:hover {
          background: unset;
          background-image: linear-gradient(to right, #ffefba, #e7e4e4);
          box-shadow: rgba(14, 63, 126, 0.04) 0px 0px 0px 1px,
            rgba(42, 51, 69, 0.04) 0px 1px 1px -0.5px,
            rgba(42, 51, 70, 0.04) 0px 3px 3px -1.5px,
            rgba(42, 51, 70, 0.04) 0px 6px 6px -3px,
            rgba(14, 63, 126, 0.04) 0px 12px 12px -6px,
            rgba(14, 63, 126, 0.04) 0px 24px 24px -12px;
        }
        .heading {
          gap: 6px;

          .icon {
            font-size: 16px;
          }
          .icon-vue {
            color: #1dcf2c;
          }
          .text {
            font-size: 14px;
            font-weight: 600;
          }
        }
        .desc {
          color: #000;
          font-size: 14px;
        }
      }
    }
  }
}
.stack {
  padding: 20px;
  background: #fff;
  &-home {
    .heading-detail {
      display: flex;
      align-items: center;
      gap: 10px;
      h2 {
        font-size: 16px;
        line-height: 22px;
        font-weight: 600;
      }
      .line {
        width: 10%;
        height: 2px;
        background: #ff512f;
      }
    }
    .list-skill {
      display: flex;
      justify-content: start;
      flex-wrap: wrap;
      align-items: center;
      gap: 10px;
      .skill-container {
        display: flex;
        justify-content: flex-start;
        align-items: end;
        padding: 12px;
        background: #f2f7fc;
        border-radius: 6px;
        transition: all 0.2s linear;
        cursor: pointer;
        &:hover {
          background: unset;
          background-image: linear-gradient(to right, #ffefba, #e7e4e4);
          box-shadow: rgba(14, 63, 126, 0.04) 0px 0px 0px 1px,
            rgba(42, 51, 69, 0.04) 0px 1px 1px -0.5px,
            rgba(42, 51, 70, 0.04) 0px 3px 3px -1.5px,
            rgba(42, 51, 70, 0.04) 0px 6px 6px -3px,
            rgba(14, 63, 126, 0.04) 0px 12px 12px -6px,
            rgba(14, 63, 126, 0.04) 0px 24px 24px -12px;
        }

        .icon {
          font-size: 16px;
        }
        .images {
          max-width: 20px;
          img {
            max-width: 100%;
          }
        }
        .name {
          margin-left: 6px;
          font-size: 16px;
          font-weight: 600;
        }
      }
    }
  }
}
.education {
  padding: 20px;
  background: #fff;
  &-home {
    .heading-detail {
      display: flex;
      align-items: center;
      gap: 10px;
      h2 {
        font-size: 16px;
        line-height: 22px;
        font-weight: 600;
      }
      .line {
        width: 10%;
        height: 2px;
        background: #ff512f;
      }
    }
  }
  .edu-card {
    padding: 20px;
    background: #f2f7fc;
    .heading {
      font-size: 14px;
      font-weight: 600;
    }
    .time {
      color: #000;
    }
  }
}
.education {
  padding: 20px;
  background: #fff;
  &-home {
    .heading-detail {
      display: flex;
      align-items: center;
      gap: 10px;
      h2 {
        font-size: 16px;
        line-height: 22px;
        font-weight: 600;
      }
      .line {
        width: 10%;
        height: 2px;
        background: #ff512f;
      }
    }
  }
}
.exp {
  padding: 20px;
  background: #fff;
  &-home {
    .heading-detail {
      display: flex;
      align-items: center;
      gap: 10px;
      h2 {
        font-size: 16px;
        line-height: 22px;
        font-weight: 600;
      }
      .line {
        width: 10%;
        height: 2px;
        background: #ff512f;
      }
    }
  }
  &-container {
    position: relative;
    .line {
      position: absolute;
      height: 100%;
      width: 2px;
      background-color: #ff512f;
      top: 0;
      left: 0;
    }
    .card-exp {
      display: flex;
      justify-content: flex-start;
      align-items: center;
      margin-left: -4px;
      gap: 10px;
      .dot {
        width: 10px;
        height: 10px;
        border-radius: 50%;
        background: #ff512f;
      }
      .content {
        padding: 20px;
        width: 100%;
        background: #f2f7fc;
        border-radius: 6px;
        .heading {
          display: flex;
          justify-content: space-between;
          align-items: center;
          .name {
            font-size: 14px;
            font-weight: 600;
          }
          .time {
            font-size: 14px;
            font-weight: 600;
          }
        }
      }
      .desc {
        font-size: 14px;
      }
    }
  }
}
</style>
