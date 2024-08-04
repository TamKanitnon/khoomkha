<template>
<div>
    <Header></Header>

    <div class="container-full">
        <div class="container">
            <h4>หน้าแรก <i class="bi bi-chevron-right"></i> <span>ลืมรหัสผ่าน</span></h4>

            <div class="form-forgot">
                <div class="left">
                    <img src="../public/images/banner-pic2.png" width="460">
                </div>

                <div class="right">
                    <h2>ตั้งรหัสผ่านใหม่</h2>
                    <p>ใช้อักขระ 8 ตัวขึ้นไป ที่มีตัวอักษร ตัวเลข และสัญลักษณ์ผสมกัน</p>
                    <div class="input-form username">
                        <label>รหัสผ่านใหม่*</label>
                        <input type="text" placeholder="กรอกรหัสผ่านใหม่">
                        <input type="text" placeholder="กรอกยืนยันรหัสผ่านใหม่">
                    </div>
                    <button class="btn-submit" @click="navigateTo('/')">ยืนยัน</button>
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

    
    .form-forgot {
        display: flex;
        align-items: center;
        justify-content: space-evenly;
    }
    .form-forgot .right {
        width: 400px;
    }
    .form-forgot .right h2 {
        color: #28c928;
        font-weight: 600;
        margin-bottom: 7px;
    }
    .form-forgot .right p {
        font-size: 12px;
        margin-bottom: 25px;
    }
    .form-forgot .right p a {
        color: #28c928;
    }
    .form-forgot .right .input-form label {
        font-size: 12px;
        display: block;
        margin-bottom: 7px;
    }
    .form-forgot .right .input-form input {
        width: 100%;
        padding: 8px;
        border: 1px solid #ababc2;
        border-radius: 5px;
        font-size: 13px;
        outline: none;
        margin-bottom: 15px;
    }
    .form-forgot .right .username {
        margin-bottom: 30px;
    }
    .form-forgot .right .btn-submit {
        width: 100%;
        height: 40px;
        border-radius: 5px;
        border: 0;
        background: #28c928;
        color: white;
        cursor: pointer;
        transition: all 100ms ease;
    }
    .form-forgot .right .btn-submit:hover {
        background: #1fbb1f;
    }
    .form-forgot .right .btn-submit:active {
        transform: scale(0.98);
    }
</style>