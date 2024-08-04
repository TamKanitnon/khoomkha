<template>
<div class="footer">
    <div class="footer-top">
        <div class="container">
            <h4>Text</h4>
            <textarea rows="4" cols="40" placeholder="What do you think about our products and services?"></textarea>
        </div>
    </div>

    <div class="footer-middle">
        <div class="container">
            <div class="contact">
                <img src="../public/images/do-you-need-help.png" width="280">
                <div class="telephone">
                    <div class="icon"><i class="bi bi-telephone-outbound"></i></div>
                    <div>
                        <p>Monday-Friday: 8am - 9pm</p>
                        <h3>080-030-0353</h3>
                    </div>
                </div>
                <div class="email">
                    <div class="icon"><i class="bi bi-envelope"></i></div>
                    <div>
                        <p>Need help with your order?</p>
                        <h5>info@khoomkha.com</h5>
                    </div>
                </div>
            </div>
            <div class="help">
                <h5>ศูนย์ช่วยเหลือ</h5>
                <a href="#">สั่งซื้อสินค้าอย่างไร</a>
                <a href="#">เริ่มขายสินค้าอย่างไร</a>
                <a href="#">ช่องทางการชำระเงิน</a>
                <a href="#">การจัดส่งสินค้า</a>
                <a href="#">การคืนเงิน/คืนสินค้า</a>
                <a href="#">ติดต่อ Khoomkha</a>
            </div>
            <div class="khoomkha">
                <h5>Khoomkha</h5>
                <a href="#">เกี่ยวกับเรา</a>
                <a href="#">ร่วมงานกับเรา</a>
                <a href="#">Market Centre</a>
                <a href="#">Seller Centre</a>
                <a href="#">นโยบายของ Khoomkha</a>
                <a href="#">ข้อกำหนดและเงื่อนไข</a>
            </div>
            <div class="download">
                <h5>ดาวน์โหลดแอปพลิเคขั่น</h5>
                <img src="../public/images/google-play.png" width="132">
                <img src="../public/images/app-store.png" width="132">
            </div>
            <div class="follow">
                <h5>ติดตามเราได้ที่</h5>
                <div>
                    <div class="icon"><i class="bi bi-facebook"></i></div>
                    <div class="icon"><i class="bi bi-twitter"></i></div>
                    <div class="icon"><i class="bi bi-instagram"></i></div>
                </div>
            </div>
        </div>
    </div>

    <div class="footer-bottom">
        <div class="container">
            <div class="left">
                <p>Copyright 2024 &copy; Khoomkha</p>
            </div>
            <div class="right">
                <a href="#">ข้อกำหนดและเงื่อนไข</a>
                <a href="#">นโยบายของ Khoomkha</a>
                <a href="#">ติดตามคำสั่งซื้อ</a>
            </div>
        </div>
    </div>
</div>
</template>

<script>

</script>

<style scoped>
    .footer {
        background: url('../public/images/banner-footer.png');
        background-size: cover;
        background-repeat: no-repeat;
        background-position: top center;
        width: 100%;
        height: 636px;
        position: relative;
    }
    .footer-top {
        display: flex;
        justify-content: center;
    }
    .footer-top .container {
        width: 1300px;
        border-bottom: 1px solid #d3cbcb;
        padding: 40px 0 10px 0;
    }
    .footer-top textarea {
        margin-top: 10px;
        border: none;
        outline: none;
        background: transparent;
        padding: 2px;
    }
    .footer-top textarea:focus {
        border: 1px solid #ece7e7;
    }
    

    .footer-middle {
        display: flex;
        justify-content: center;
    }
    .footer-middle .container {
        width: 1300px;
        display: flex;
        justify-content: space-between;
        gap: 40px;
        padding-top: 40px;
    }
    .footer-middle .contact .telephone,
    .footer-middle .contact .email {
        display: flex;
        align-items: center;
        gap: 25px;
        margin-top: 20px;
    }
    .footer-middle .contact i {
        font-size: 25px;
    }
    .footer-middle .contact p {
        font-size: 13px;
        color: #665e5e;
    }
    .footer-middle .help,
    .footer-middle .khoomkha {
        display: flex;
        flex-direction: column;
    }
    .footer-middle .help h5,
    .footer-middle .khoomkha h5 {
        margin-bottom: 20px;
    }
    .footer-middle .help a,
    .footer-middle .khoomkha a {
        font-size: 14px;
        margin-bottom: 4px;
    }
    .footer-middle .download {
        display: flex;
        flex-direction: column;
    }
    .footer-middle .download h5 {
        margin-bottom: 20px;
    }
    .footer-middle .download img {
        margin-bottom: 10px;
        cursor: pointer;
        transition: all 200ms ease;
    }
    .footer-middle .download img:hover {
        transform: scale(1.03);
    }
    .footer-middle .follow h5 {
        margin-bottom: 20px;
        text-align: center;
    }
    .footer-middle .follow div {
        display: flex;
        justify-content: space-between;
        gap: 6px;
    }
    .footer-middle .follow .icon {
        background: white;
        width: 35px;
        height: 35px;
        border-radius: 5px;
        display: flex;
        justify-content: center;
        align-items: center;
        cursor: pointer;
        box-shadow: 0px 0px 5px 0px rgba(0, 0, 0, 0.3); 
        transition: all 200ms ease;
    }
    .footer-middle .follow .icon:hover {
        background: #f0f0f3;
    }
    .footer-middle .follow div .icon:nth-child(1) {
        color: #0000ff;
        font-size: 17px;
    }
    .footer-middle .follow div .icon:nth-child(2) {
        color: #00b7ff;
        font-size: 17px;
    }
    .footer-middle .follow div .icon:nth-child(3) {
        color: #dd0c0c;
        font-size: 17px;
    }


    .footer-bottom {
        width: 100%;
        height: 60px;
        display: flex;
        justify-content: center;
        align-items: center;
        position: absolute;
        bottom: 0;
    }
    .footer-bottom .container {
        width: 1300px;
        display: flex;
        justify-content: space-between;
    }
    .footer-bottom .left p {
        font-size: 14px;
    }
    .footer-bottom .right a {
        margin-left: 15px;
        font-size: 14px;
    }
</style>