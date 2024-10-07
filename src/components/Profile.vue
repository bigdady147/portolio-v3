<template>
  <div  class="profile-block">
    <div class="avatar"></div>
    <div class="name d-flex justify-content-center align-items-center mt-3">
      <h2>Nguyen Truong An</h2>
    </div>
    <div class="title d-flex justify-content-center align-items-center">
      <span>FrontEnd Developer</span>
    </div>
    <div class="social">
      <a href="https://www.facebook.com/Prog.ichi/">
        <div class="btn-social">
          <div class="icon">
            <i class="fa-brands fa-facebook-f"></i>
          </div>
        </div>
      </a>
      <a href="https://www.linkedin.com/in/an-nguyen-truong-a21681216/">
        <div class="btn-social">
          <div class="icon">
            <i class="fa-brands fa-linkedin-in text-primary"></i>
          </div>
        </div>
      </a>
      <a href="https://github.com/bigdady147?tab=repositories">
        <div class="btn-social">
          <div class="icon">
            <i class="fa-brands fa-github text-dark"></i>
          </div>
        </div>
      </a>
      <!-- <a href="https://gitlab.com/annt9">
        <div class="btn-social">
          <div class="icon">
            <i style="color: orange" class="fa-brands fa-git-alt"></i>
          </div>
        </div>
      </a> -->
    </div>
    <div class="infor">
      <div class="btn-infor">
        <div class="icon  text-primary">
          <i class="fa-solid fa-mobile-screen "></i>
        </div>
        <div class="des">
          <div class="label">Phone</div>
          <div class="content">+84 848123437</div>
        </div>
      </div>
      <div class="btn-infor mt-2">
        <div class="icon text-warning">
          <i class="fa-regular fa-envelope"></i>

        </div>
        <div class="des">
          <div class="label">Email</div>
          <div class="content">truongan.dev3010@gmail.com</div>
        </div>
      </div>
      <div class="btn-infor mt-2">
        <div class="icon">
          <i class="fa-solid fa-location-dot text-danger"></i>
          
        </div>
        <div class="des">
          <div class="label">Location</div>
          <div class="content">Ho Chi Minh City, Vietnam</div>
        </div>
      </div>
    </div>
    <div class="action">
      <a href="/cv/cv.pdf" download>
        <div class="btn btn-sm download">Download Resume</div>
      </a>
    </div>
  </div>
</template>

<script setup>



</script>
<style lang="scss">
.profile-block {
  background: #fff;
  position: relative;
  min-height: 300px;
  border-radius: 6px;
  padding: 30px 0px;
  .avatar {
    width: 190px;
    height: 200px;
    background: url("/images/avatar.jpg");
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    border-radius: 6px;
    display: block;
    margin: 0 auto;
  }
  .name {
    h2 {
      font-size: 26px;
      line-height: 32px;
      font-weight: 600;
    }
  }
  .title {
    span {
      font-size: 16px;
      line-height: 24px;
      color: #8b8888;
    }
  }
  .social {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 10px;
    padding: 20px 20px 0px 20px;
    .btn-social {
      width: 46px;
      height: 46px;
      background-color: #f2f7fc;
      border-radius: 6px;
      display: flex;
      justify-content: center;
      align-items: center;
      transition: all 0.2s linear;
      &:hover {
        background-image: linear-gradient(to right, #ffefba, #ffffff);
        background-color: unset;
        box-shadow: rgba(14, 63, 126, 0.04) 0px 0px 0px 1px,
          rgba(42, 51, 69, 0.04) 0px 1px 1px -0.5px,
          rgba(42, 51, 70, 0.04) 0px 3px 3px -1.5px,
          rgba(42, 51, 70, 0.04) 0px 6px 6px -3px,
          rgba(14, 63, 126, 0.04) 0px 12px 12px -6px,
          rgba(14, 63, 126, 0.04) 0px 24px 24px -12px;
      }
      .icon {
        i {
          color: rgb(13, 90, 235);
          font-size: 14px;
        }
      }
    }
  }
  .infor {
    padding: 20px 20px 0px 20px;

    .btn-infor {
      display: flex;
      justify-content: flex-start;
      align-items: center;
      padding: 10px 10px;
      border-radius: 6px;
      background: #f2f7fc;
      transition: all 0.2s linear;

      &:hover {
        background: unset;

        background-image: linear-gradient(to right, #ffefba, #ffffff);
        box-shadow: rgba(14, 63, 126, 0.04) 0px 0px 0px 1px,
          rgba(42, 51, 69, 0.04) 0px 1px 1px -0.5px,
          rgba(42, 51, 70, 0.04) 0px 3px 3px -1.5px,
          rgba(42, 51, 70, 0.04) 0px 6px 6px -3px,
          rgba(14, 63, 126, 0.04) 0px 12px 12px -6px,
          rgba(14, 63, 126, 0.04) 0px 24px 24px -12px;
      }
      .icon {
        width: 40px;
        display: flex;
        justify-content: center;
        align-items: center;
        i {
          font-size: 16px;
        }
      }
      .des {
        font-size: 14px;

        .label {
          color: #8b8888;
        }
        .content {
          color: #000;
          font-weight: 600;
        }
      }
    }
  }
  .action {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 20px 20px 0px 20px;
    .download {
      padding: 12px 32px;
      background-image: linear-gradient(to right, #ff512f, #f09819);
      border-radius: 6px;
      color: #fff;
      font-size: 14px;
      font-weight: 600;
      transition: all 0.2s ease;
      &:hover {
        box-shadow: rgba(0, 0, 0, 0.45) 0px 25px 20px -20px;
      }
    }
  }
}

</style>
