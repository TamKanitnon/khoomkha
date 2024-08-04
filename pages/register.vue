<template>
<div>
    <Header></Header>

    <div class="container-full">
        <div class="container">
            <h4>หน้าแรก <i class="bi bi-chevron-right"></i> <span>สมัครสมาชิก</span></h4>

            <div class="create-account">
                <div class="title">
                    <h2>สร้างบัญชี Khoomkha</h2>
                    <p>เป็นสมาชิกอยู่แล้ว ? <a @click="navigateTo('/')">เข้าสู่ระบบ</a> ที่นี้</p>
                </div>
                <div class="form-register">
                    <div class="left">
                        <div class="input-form">
                            <label>ข้อมูลสมาชิก*</label>
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
                            <label>SMS รหัสยืนยันตัวตน*</label>
                            <input type="text" placeholder="กรอกตัวเลข 6 หลัก">
                        </div>
                        <div class="input-form">
                            <label>SMS รหัสยืนยันตัวตน*</label>
                            <input type="text" placeholder="กรอกตัวเลข 6 หลัก">
                        </div>
                        <div class="btn-submit">
                            <button>สมัครสมาชิก</button>
                        </div>
                        <div class="other-register">
                            <button class="btn-other-register"><i class="bi bi-facebook"></i> Facebook</button>
                            <button class="btn-other-register"><img src="../public/images/logo-google.png" width="20"> Google</button>
                        </div>
                    </div>
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
    .container-full h4 span {
        color: #28c928;
    }
</style>