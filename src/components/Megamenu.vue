<script setup>
</script>
<template>
    <div class="menubar__megamenu absolute top-0 left-0 right-0 h-[500px]
     bg-white mt-[100px]
        p-[70px] z-[2] scale-x-1 scale-y-0 transition-transform 
        ease-linear duration-100 shadow-md">
        <div class="w-[1200px] my-0 mx-auto">
            <div class="flex justify-between gap-5">
                <div class="megamenu-column">
                    <h4>home page1</h4>
                    <div>home1</div>
                    <div class="w-full">
                        <span class="w-[50%]">home2</span>
                        <span class="ml-1"></span>
                        <span class="h-full w-[50%] inline-block">
                            <a class="inline-flex justify-center w-full h-full p-0 px-2 py-1 m-auto text-sm text-center text-white bg-red-500 border-red-700 border-solid rounded-lg border-1"><span>new!</span> </a>
                        </span>
                    </div>
                    <div>home3</div>
                    <div>
                        <span>home2</span>
                        <span class="ml-1"></span>
                        <span><a class="bg-red-500 px-2 py-1 border-red-700 text-sm border-solid rounded-lg border-1 p-0 mr-[20px] w-[20px] h-[10px] text-center text-white">new!</a></span>
                    </div>
                    <div>home5</div>
                </div>

                <div class="megamenu-column">
                    <h4>home page2</h4>
                    <div>home1</div>
                    <div>home2</div>
                    <div>home3</div>
                    <div>home4</div>
                    <div>home5</div>
                </div>

                <div class="megamenu-column">
                    <h4>home page3</h4>
                    <div>home1</div>
                    <div>home2</div>
                    <div>home3</div>
                    <div>home4</div>
                    <div>home5</div>
                </div>

                <div class="megamenu-column">
                    <h4>home page4</h4>
                    <div>home1</div>
                    <div>home2</div>
                    <div>home3</div>
                    <div>home4</div>
                    <div>home5</div>
                </div>
                <div>
                    <div class="flex justify-between cursor-pointer p-[26px] bg-blue-100">
                        <div class="image_holder__desc">
                            <h5>sale collection</h5>
                            <p class="text-4xl font-bold break-normal">up to 80% off retail</p>
                            <div class="inline megamenue__ column2__show hover:rounded-xl hover:inline-block">
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
/* .menubar__megamenu {
    position: absolute;
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
} */

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
    background-color: rgb(231, 234, 237);
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