<template>
    <div class="width-33">
        <div>
            <b class="item-title">Lorem ipsum dolor sit amet</b>
            <div class="item-content">
                <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTA9jyeynlFwVGBRreQHauSuqrkhoKGk7ytIw8OpgZbNA&s"
                    alt="" class="img-content">
                <p class="item-sub">
                    Lorem ipsum dolor sit
                    amet, consectetur
                    adipiscing elit. Sed
                    dui sodales, faucibus
                    libero ut, posuere felis.
                    Donec imperdiet suscipit
                    accumsan. Aenean
                    consequat condimentum velit ut tempor. Nam
                    porta massa in metus bibendum congue.
                    Pellentesque ultrices vestibulum mattis.
                    Aliquam egestas nunc at ullamcorper ultricies.
                    Donec feugiat velit nulla, vel sodales est
                    jullamcorper id.
                </p>
            </div>
        </div>
    </div>
</template>

<style>
.width-33 {
    max-width: 32%;
    margin-top: 20px;
}

.item-title {
    width: 100%;
    float: left;
    font-size: 1.2rem;
    text-align: start;
    padding: 10px 0;
}

.img-content {
    width: 83px;
    float: left;
    height: 95px;
    margin-right: 20px;
}

.item-sub {
    margin: 0;
    text-align: initial;
}

@media screen and (min-width: 320px) and (max-width: 767px){
    .width-33 {
        max-width: 100% !important;
    }
}

@media  screen and (min-width: 768px) and (max-width: 1200px) {
    .width-33 {
        max-width: 48% !important
    }
}

</style>