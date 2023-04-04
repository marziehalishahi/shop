<script setup>
</script>
<template>
    <div class="menubar__megamenu megamenu">
        <div class="megamenu_container">
            <div class="flex justify-between gap-5">
                <div class="megamenu__column">
                    <h4>home page1</h4>
                    <div>home1</div>
                    <div>
                        <span>home2</span>
                        <span class="ml-1"></span>
                        <span><a class="megamenu__column_home_new">new!</a></span>
                    </div>
                    <div>home3</div>
                    <div>
                        <span>home2</span>
                        <span class="ml-1"></span>
                        <span><a class="megamenu__column_home_new">new!</a></span>
                    </div>
                    <div>home5</div>
                </div>

                <div class="megamenu__column">
                    <h4>home page2</h4>
                    <div>home1</div>
                    <div>home2</div>
                    <div>home3</div>
                    <div>home4</div>
                    <div>home5</div>
                </div>

                <div class="megamenu__column">
                    <h4>home page3</h4>
                    <div>home1</div>
                    <div>home2</div>
                    <div>home3</div>
                    <div>home4</div>
                    <div>home5</div>
                </div>

                <div class="megamenu__column">
                    <h4>home page4</h4>
                    <div>home1</div>
                    <div>home2</div>
                    <div>home3</div>
                    <div>home4</div>
                    <div>home5</div>
                </div>
                <div>
                    <div class="megamenu_image_holder image_holder">
                        <div class="image_holder__desc">
                            <h5>sale collection</h5>
                            <p class="text-4xl font-bold break-normal">up to 80% off retail</p>
                            <div class="megamenue__ column2__show">
                                <a class="column2__show">show me all</a>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between mb-4 image__holder_container">
                                <div><img class="object-contain w-[225px] h-auto" src="../../images/12.jpg"></div>
                            </div>

                        </div>

                    </div>
                </div>
            </div>
        </div>


    </div>
</template>

<style scoped>
.menubar__megamenu {
    position: absolute;
    /* width: 100%; */
    left: 0;
    right: 0;
    height: 500px;
    background-color: white;
    top: 0;
    margin-top: 100px;
    padding: 70px;
    transform: scale(1, 0);
    transition: transform 100ms ease-in-out;
    z-index: 2;
    box-shadow: 0 4px 6px -1px rgb(0 0 0 / 0.1), 0 2px 4px -2px rgb(0 0 0 / 0.1);
}

.megamenu_container {
    width: 1200px;
    margin: 0 auto;
}

.megamenu__column {
    display: flex;
    flex-direction: column;
    /* align-items: center; */
    /* margin-left: 2rem;
    margin-right: 8rem; */
    cursor: pointer;
    gap: 1rem;
}

.megamenu__column_home_new {
    border: 1px solid none;
    border-radius: 8px;
    padding: 0px;
    margin-right: 20px;
    /* display: inline-block; */
    width: 40%;
    text-align: center;
    background-color: red;
    color: white;
    outline: red;
}

.image_holder {
    display: flex;
    justify-content: space-between;
    cursor: pointer;
    background-color: rgb(239, 244, 248);
    padding: 26px;
}

/* .image_holder__desc:nth-child(n){
    margin-top: 4px;
}
.image_holder__desc:last-child{
    margin-top: 9px;
} */
.image_holder__desc {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    /* gap: 10px; */
}

.column2__show {
    border: 1px solid none;
    border-radius: 18px;
    padding: 0px 0;
    display: inline-block;
    width: 70%;
    text-align: center;
    background-color: white;
    transform: scale(1, 1);
    transition: all 100ms linear;
    color: black;
    outline: none;
}

.column2__show:hover {
    border-radius: 18px;
    padding: 15px 0;
    display: inline-block;
    width: 70%;
    background-color: rgb(221, 221, 240);
    color: white;
    border: none;
    outline: none;
    transform: scale(1.1, 1.1);
}</style>