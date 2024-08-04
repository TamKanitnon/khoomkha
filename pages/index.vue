<template>
<div class="index">
    <Header></Header>

    <div class="container-full">
        <div class="container">
            <h4>หน้าแรก <i class="bi bi-chevron-right"></i> <span>เข้าสู่ระบบ</span></h4>
            <div class="form-components">
                <div class="form-welcome" v-if="!loginSucceed">
                    <div class="left">
                        <img src="../public/images/banner-pic1.png" width="460">
                    </div>
                    <div class="right">
                        <h2>ยินดีต้อนรับสู่ Khoomkha</h2>
                        <p>สมาชิกใหม่ ? <a href="#"><NuxtLink to="/register">ลงทะเบียน</NuxtLink></a> ที่นี้</p>
                        <div class="input-form username">
                            <label>หมายเลยโทรศัพท์หรืออีเมล*</label>
                            <input type="text" placeholder="กรอกหมายเลขโทรศัพท์หรืออีเมลของคุณ">
                        </div>
                        <div class="input-form password">
                            <label>รหัสผ่าน*</label>
                            <input type="password" placeholder="กรอกรหัสผ่าน">
                        </div>
                        <div class="forget-password"><a href="#"><NuxtLink to="/forgot-password">ลืมรหัสผ่าน ?</NuxtLink></a></div>
                        <button class="btn-submit"  @click="loginSucceed = !loginSucceed">เข้าสู่ระบบ</button>
                        <div class="label-other-login">
                            <div></div>
                            <span>หรือเข้าสู่ระบบด้วย</span>
                            <div></div>
                        </div>
                        <div class="other-login">
                            <button class="btn-other-login"><i class="bi bi-facebook"></i> Facebook</button>
                            <button class="btn-other-login"><img src="../public/images/logo-google.png" width="20"> Google</button>
                        </div>
                    </div>
                </div>
                <div class="form-succeed" v-if="loginSucceed">
                    <i class="bi bi-check-circle-fill"></i>
                    <h2>เข้าสู่ระบบสำเร็จ</h2>
                </div>
            </div>
        </div>
    </div>

    <Footer></Footer>
</div>
</template>

<script>
export default {
    data() {
        return {
            loginSucceed: false
        }
    }
}
</script>

<style>
    /* **************************** */
    @import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Prompt:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
    @import url("https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css");
    * {
        margin: 0;
        padding: 0;
        font-family: 'Prompt', sans-serif;
        box-sizing: border-box;
    }
    a {
        text-decoration: none;
        color: black;
        cursor: pointer;
    }
    a:hover {
        text-decoration: underline;
    }


    /* **************************** */
    .index .container-full {
        width: 100%;
        height: 670px;
        display: flex;
        justify-content: center;
    }
    .index .container-full .container {
        width: 1300px;
    }
    .index .container-full h4 {
        margin: 25px 0;
        color: #b6b3b3;
        font-weight: 400;
    }
    .index .container-full h4 i {
        font-size: 12px;
    }
    .index .container-full h4 span {
        color: #28c928;
    }

    
    /* **************************** */
    .index .form-welcome {
        display: flex;
        align-items: center;
        justify-content: space-evenly;
    }
    .index .form-welcome .right {
        width: 400px;
    }
    .index .form-welcome .right h2 {
        color: #28c928;
        font-weight: 600;
        margin-bottom: 7px;
    }
    .index .form-welcome .right p {
        font-size: 12px;
        margin-bottom: 25px;
    }
    .index .form-welcome .right p a {
        color: #28c928;
    }
    .index .form-welcome .right .input-form label {
        font-size: 12px;
        display: block;
        margin-bottom: 7px;
    }
    .index .form-welcome .right .input-form input {
        width: 100%;
        padding: 8px;
        border: 1px solid #ababc2;
        border-radius: 5px;
        font-size: 13px;
        outline: none;
    }
    .index .form-welcome .right .username {
        margin-bottom: 20px;
    }
    .index .form-welcome .right .password {
        margin-bottom: 5px;
    }
    .index .form-welcome .right .forget-password a {
        color: #28c928;
        font-size: 12px;
    }
    .index .form-welcome .right .forget-password {
        margin-bottom: 20px;
    }
    .index .form-welcome .right .btn-submit {
        width: 100%;
        height: 40px;
        border-radius: 5px;
        border: 0;
        background: #28c928;
        color: white;
        cursor: pointer;
        transition: all 100ms ease;
    }
    .index .form-welcome .right .btn-submit:hover {
        background: #1fbb1f;
    }
    .index .form-welcome .right .btn-submit:active {
        transform: scale(0.98);
    }
    .index .form-welcome .right .label-other-login {
        height: 65px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .index .form-welcome .right .label-other-login span {
        width: 320px;
        text-align: center;
        font-size: 12px;
        color: #ababc2;
    }
    .index .form-welcome .right .label-other-login div {
        background: #ababc2;
        width: 100%;
        height: 1px;
        text-align: center;
    }
    .index .form-welcome .right .other-login {
        display: flex;
        justify-content: space-between;
    }
    .index .form-welcome .right .btn-other-login {
        background: transparent;
        border: 1px solid #28c928;
        width: 185px;
        height: 40px;
        border-radius: 5px;
        cursor: pointer;
        color: #28c928;
        font-size: 14px;
        transition: all 100ms ease;
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 10px;
    }
    .index .form-welcome .right .btn-other-login:hover {
        background: #f1faf1;
    }
    .index .form-welcome .right .btn-other-login:active {
        transform: scale(0.97);
    }
    .index .form-welcome .right .btn-other-login i {
        color: #2264f3;
        font-size: 18px;
    }


    /* **************************** */
    .index .form-succeed {
        display: flex;
        height: 500px;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        color: #1eb31e;
    }
    .index .form-succeed i {
        font-size: 140px;
    }
    .index .form-succeed h2 {
        font-weight: 400;
        margin-top: -30px;
    }
</style>