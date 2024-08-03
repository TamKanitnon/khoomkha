<template>
<div class="index">
    <Header></Header>

    <div class="container-full">
        <div class="container">
            <h4>หน้าแรก <i class="bi bi-chevron-right"></i> <span>เข้าสู่ระบบ</span></h4>
            <div class="input-from">
                <div class="welcome">

                </div>
            </div>
        </div>
    </div>

    <Footer></Footer>
</div>
</template>

<script>

</script>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Prompt:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
    @import url("https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css");
    * {
        margin: 0;
        padding: 0;
        font-family: 'Prompt', sans-serif;
    }
    a {
        text-decoration: none;
        color: black;
    }
    a:hover {
        text-decoration: underline;
    }


    .index .container-full {
        width: 100%;
        height: 600px;
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
</style>