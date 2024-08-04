<template>
<div>
    <div class="header-top">
        <div class="container">
            <div class="left">
                <p>We deliver to you every day from <span>7:00 to 23:00</span></p>
            </div>
            <div class="right">
                <a href="#">Seller Centre</a>
                <a href="#">ช้อปบนแอปของเรา</a>
                <a href="#">ติดตามสินค้า</a>
                <a href="#">ข่วยเหลือ</a>
                <a href="#"><Nuxtlink to="/">เปลี่ยนภาษา</Nuxtlink></a>
            </div>
        </div>
    </div>

    <div class="header-bottom">
        <div class="container">
            <img src="../public/images/khoomkha-logo.PNG" width="227px" style="cursor: pointer;" @click="navigateTo('/')">
            <div class="search">
                <input type="search" placeholder="ค้นหาสินค้า ผลิตภัณฑ์ หมวดหมู่ หรือแบรนด์...">
                <i class="bi bi-search"></i>
            </div>
            <div class="username">
                <div class="icon">
                    <i class="bi bi-person-fill"></i>
                </div>
                <div>
                    <p>ยินดีต้อนรับ</p>
                    <h5>USERNAME</h5>
                </div>
            </div>
            <div class="basket">
                <div class="icon">
                    <i class="bi bi-cart-fill"></i>
                    <div class="item">5</div>
                </div>
                <div>
                    <p>ตะกร้าของฉัน</p>
                    <h5>$1,689.00</h5>
                </div>
            </div>
        </div>
    </div>
</div>
</template>

<script>

</script>

<style scoped>
    .header-top {
        width: 100%;
        height: 40px;
        display: flex;
        justify-content: center;
        border-bottom: 1px solid #f5efef;
    }
    .header-top .container {
        width: 1300px;
        display: flex;
        justify-content: space-between;
    }
    .header-top .left {
        display: flex;
        align-items: center;
        gap: 13px;
        color: #474545;
        font-size: 13px;
    }
    .header-top .left span {
        color: #ff4800;
    }
    .header-top .right {
        display: flex;
        align-items: center;
        gap: 35px;
    }
    .header-top .right a {
        font-size: 13px;
    }


    .header-bottom {
        width: 100%;
        display: flex;
        justify-content: center;
        height: 65px;
        box-shadow: 0px 5px 5px 0px rgba(0, 0, 0, 0.05); 
    }
    .header-bottom .container {
        width: 1300px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .header-bottom .search {
        background: #f5f4f4;
        width: 450px;
        height: 40px;
        border-radius: 20px;
        overflow: hidden;
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 0 15px;
    }
    .search input {
        border: 0;
        background: transparent;
        width: 90%;
        padding: 0 5px;
        outline: none;
    }
    .search i {
        cursor: pointer;
    }
    .header-bottom .username {
        display: flex;
        align-items: center;
        gap: 10px;
    }
    .header-bottom .username .icon {
        width: 40px;
        height: 40px;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        background: #f5f2f2;
    }
    .header-bottom .username i {
        font-size: 24px;
        color: #28c928;
    }
    .header-bottom .username p {
        font-size: 13px;
        color: #665e5e;
    }
    .header-bottom .basket {
        display: flex;
        align-items: center;
        gap: 10px;
    }
    .header-bottom .basket .icon div {
        background: #28c928;
        font-size: 12px;
        width: 15px;
        height: 15px;
        border-radius: 50%;
        display: flex;
        justify-content: center;
        align-items: center;
        color: white;
        font-weight: 300;
        position: absolute;
        bottom: -5px;
        right: -5px;
    }
    .header-bottom .basket .icon {
        width: 40px;
        height: 40px;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        background: #f5f2f2;
        position: relative;
    }
    .header-bottom .basket i {
        font-size: 20px;
        color: #28c928;
    }
    .header-bottom .basket p {
        font-size: 13px;
        color: #665e5e;
    }
</style>