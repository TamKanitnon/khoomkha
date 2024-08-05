<template>
<div>
    <Header></Header>

    <div class="container-full">
        <div class="container">
            <h4>หน้าแรก <i class="bi bi-chevron-right"></i> <span>สมัครสมาชิก</span></h4>

            <div class="create-account" v-if="!registerSucceed">
                <div class="title">
                    <h2>สร้างบัญชี Khoomkha</h2>
                    <p>เป็นสมาชิกอยู่แล้ว ? <a @click="navigateTo('/')">เข้าสู่ระบบ</a> ที่นี้</p>
                </div>
                <div class="form-register">
                    <div class="left">
                        <div class="input-form">
                            <label>ข้อมูลสมาชิก*</label>
                            <select v-model="memberType">
                                <option value="personal">บุคคลทั่วไป</option>
                                <option value="entrepreneur">ผู้ประกอบการ</option>
                            </select>
                        </div>
                        <div class="input-form">
                            <label>หมายเลขโทรศัพท์หรืออีเมล*</label>
                            <input type="text" placeholder="กรอกหมายเลขโทรศัพท์หรืออีเมลของคุณ">
                        </div>
                        <div class="input-form">
                            <label>SMS รหัสยืนยันตัวตน*</label>
                            <input type="text" placeholder="กรอกตัวเลข 6 หลัก">
                        </div>
                        <div class="input-form">
                            <label>รหัสผ่าน*</label>
                            <input type="password" placeholder="กรอกรหัสผ่าน">
                        </div>
                    </div>

                    <div class="right">
                        <div class="input-form">
                            <label>ชื่อผู้ใช้*</label>
                            <input type="text" placeholder="กรอกชื่อผู้ใช้">
                        </div>
                        <div class="input-form">
                            <label>ชื่อจริง-นามสกุล*</label>
                            <input type="text" placeholder="กรอกชื่อจริง-นามสกุล">
                        </div>
                        <div>
                            <button class="btn-submit" @click="registerSucceed = !registerSucceed">สมัครสมาชิก</button>
                        </div>
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
            </div>

            <div class="form-succeed" v-if="registerSucceed">
                <i class="bi bi-check-circle-fill"></i>
                <h2>สมัครสมาชิกสำเร็จ</h2>
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
            memberType: 'personal',
            registerSucceed: false
        }
    }
}
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
    .container-full span {
        color: #28c928;
    }
    .create-account {
        margin-top: 55px;
        display: flex;
        flex-direction: column;
        gap: 30px;
        align-items: center;
    }
    .create-account .title {
        width: 850px;
    }
    .create-account .title h2 {
        font-weight: 600;
        font-size: 26px;
        color: #28c928;
        margin-bottom: 7px;
    }
    .create-account .title p {
        font-size: 13px;
    }
    .create-account .title a {
        color: #28c928;
    }
    .create-account .form-register {
        display: flex;
        justify-content: space-between;
        gap: 45px;
        width: 850px;
    }
    .create-account .form-register .left,
    .create-account .form-register .right {
        width: 100%;
    }
    .create-account .form-register .input-form {
        margin-bottom: 22px;
    }
    .create-account .form-register .input-form label {
        font-size: 12px;
        display: block;
        margin-bottom: 8px;
    }
    .create-account .form-register .input-form input {
        width: 100%;
        padding: 8px;
        border: 1px solid #ababc2;
        border-radius: 5px;
        font-size: 13px;
        outline: none;
    }
    .create-account .form-register .input-form select {
        width: 100%;
        padding: 8px;
        border: 1px solid #ababc2;
        border-radius: 5px;
        font-size: 13px;
        outline: none;
        cursor: pointer;
    }
    .create-account .form-register .btn-submit {
        width: 100%;
        height: 40px;
        border-radius: 5px;
        border: 0;
        background: #28c928;
        color: white;
        cursor: pointer;
        transition: all 100ms ease;
        margin-top: 6px;
    }
    .create-account .form-register .btn-submit:hover {
        background: #1fbb1f;
    }
    .create-account .form-register .btn-submit:active {
        transform: scale(0.98);
    }
    .create-account .form-register .label-other-login {
        height: 65px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .create-account .form-register .label-other-login span {
        width: 320px;
        text-align: center;
        font-size: 12px;
        color: #ababc2;
    }
    .create-account .form-register .label-other-login div {
        background: #ababc2;
        width: 100%;
        height: 1px;
        text-align: center;
    }
    .create-account .form-register .other-login {
        display: flex;
        justify-content: space-between;
    }
    .create-account .form-register .btn-other-login {
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
    .create-account .form-register .btn-other-login:hover {
        background: #f1faf1;
    }
    .create-account .form-register .btn-other-login:active {
        transform: scale(0.97);
    }
    .create-account .form-register .btn-other-login i {
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