<template>
<div>
    <Header></Header>

    <div class="container-full">
        <div class="container">
            <h4>หน้าแรก <i class="bi bi-chevron-right"></i> <span>เข้าสู่ระบบ</span></h4>
            <div class="form-components">
                <div class="form-welcome" v-if="!loginSucceed">
                    <div class="left">
                        <img src="~/assets/images/banner-pic1.png" width="460">
                    </div>
                    <div class="right">
                        <h2>ยินดีต้อนรับสู่ Khoomkha</h2>
                        <p>สมาชิกใหม่ ? <a @click="navigateTo('/register')">ลงทะเบียน</a> ที่นี้</p>
                        <div class="input-form username">
                            <label>หมายเลยโทรศัพท์หรืออีเมล*</label>
                            <input type="text" placeholder="กรอกหมายเลขโทรศัพท์หรืออีเมลของคุณ">
                        </div>
                        <div class="input-form password">
                            <label>รหัสผ่าน*</label>
                            <input type="password" placeholder="กรอกรหัสผ่าน">
                        </div>
                        <div class="forget-password"><a @click="navigateTo('/forgot-password')">ลืมรหัสผ่าน ?</a></div>
                        <button class="btn-submit"  @click="loginSucceed = !loginSucceed">เข้าสู่ระบบ</button>
                        <div class="label-other-login">
                            <div></div>
                            <span>หรือเข้าสู่ระบบด้วย</span>
                            <div></div>
                        </div>
                        <div class="other-login">
                            <button class="btn-other-login"><i class="bi bi-facebook"></i> Facebook</button>
                            <button class="btn-other-login"><img src="~/assets/images/logo-google.png" width="20"> Google</button>
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

<script setup lang="ts">
const loginSucceed = ref(false);

console.log("show me the money", loginSucceed.value)
</script>

<style scoped>
    .container-full {
        width: 100%;
        height: 670px;
        display: flex;
        justify-content: center;
    }
    .container-full .container {
        width: 1300px;
    }
    .container-full h4 {
        margin: 25px 0;
        color: #b6b3b3;
        font-weight: 400;
    }
    .container-full h4 i {
        font-size: 12px;
    }
    .container-full h4 span {
        color: #28c928;
    }
    .form-welcome {
        display: flex;
        align-items: center;
        justify-content: space-evenly;
    }
    .form-welcome .right {
        width: 400px;
    }
    .form-welcome .right h2 {
        color: #28c928;
        font-weight: 600;
        margin-bottom: 7px;
    }
    .form-welcome .right p {
        font-size: 12px;
        margin-bottom: 25px;
    }
    .form-welcome .right p a {
        color: #28c928;
    }
    .form-welcome .right .input-form label {
        font-size: 12px;
        display: block;
        margin-bottom: 7px;
    }
    .form-welcome .right .input-form input {
        width: 100%;
        padding: 8px;
        border: 1px solid #ababc2;
        border-radius: 5px;
        font-size: 13px;
        outline: none;
    }
    .form-welcome .right .username {
        margin-bottom: 20px;
    }
    .form-welcome .right .password {
        margin-bottom: 5px;
    }
    .form-welcome .right .forget-password a {
        color: #28c928;
        font-size: 12px;
    }
    .form-welcome .right .forget-password {
        margin-bottom: 20px;
    }
    .form-welcome .right .btn-submit {
        width: 100%;
        height: 40px;
        border-radius: 5px;
        border: 0;
        background: #28c928;
        color: white;
        cursor: pointer;
        transition: all 100ms ease;
    }
    .form-welcome .right .btn-submit:hover {
        background: #1fbb1f;
    }
    .form-welcome .right .btn-submit:active {
        transform: scale(0.98);
    }
    .form-welcome .right .label-other-login {
        height: 65px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .form-welcome .right .label-other-login span {
        width: 320px;
        text-align: center;
        font-size: 12px;
        color: #ababc2;
    }
    .form-welcome .right .label-other-login div {
        background: #ababc2;
        width: 100%;
        height: 1px;
        text-align: center;
    }
    .form-welcome .right .other-login {
        display: flex;
        justify-content: space-between;
    }
    .form-welcome .right .btn-other-login {
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
    .form-welcome .right .btn-other-login:hover {
        background: #f1faf1;
    }
    .form-welcome .right .btn-other-login:active {
        transform: scale(0.97);
    }
    .form-welcome .right .btn-other-login i {
        color: #2264f3;
        font-size: 18px;
    }
    .form-succeed {
        display: flex;
        height: 500px;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        color: #1eb31e;
    }
    .form-succeed i {
        font-size: 140px;
    }
    .form-succeed h2 {
        font-weight: 400;
        margin-top: -30px;
    }
</style>