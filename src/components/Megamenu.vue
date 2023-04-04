<script setup>
</script>
<template>
    <div class="menubar__megamenu megamenu">
        <div class="flex justify-center gap-5 ">

            <div class="megamenu__column1">
                <h4>home page1</h4>
                <div>home1</div>
                <div>
                    <span class="ml-16">home2</span>
                    <span class="ml-1"></span>
                    <span><a class="megamenu__column1__home__new">new!</a></span>
                </div>
                <div>home3</div>
                <div>
                    <span class="ml-16">home2</span>
                    <span class="ml-1"></span>
                    <span><a class="megamenu__column1__home__new">new!</a></span>
                </div>
                <div>home5</div>
            </div>

            <div class="megamenu__column1">
                <h4>home page2</h4>
                <div>home1</div>
                <div>home2</div>
                <div>home3</div>
                <div>home4</div>
                <div>home5</div>
            </div>

            <div class="megamenu__column1">
                <h4>home page3</h4>
                <div>home1</div>
                <div>home2</div>
                <div>home3</div>
                <div>home4</div>
                <div>home5</div>
            </div>

            <div class="megamenu__column1">
                <h4>home page4</h4>
                <div>home1</div>
                <div>home2</div>
                <div>home3</div>
                <div>home4</div>
                <div>home5</div>
            </div>
            <div class="flex justify-between mb-3 megamenu__column2">
                <div>
                    <h5>sale collection</h5>
                    <div>
                        <p>up to 80% off retail</p>
                    </div>
                    <div class="flex justify-between mb-4 megamenue__column2__image">
                        <div><img src="../assets/images/12.jpg"></div>
                    </div>
                    <div class="megamenue__ column2__show">
                        <a class="column2__show">show me all</a>
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

.megamenu__column1 {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-left: 2rem;
    margin-right:8rem;
    cursor: pointer
}

 .megamenu__column1__home__new{
    border: 1px solid none;
    border-radius: 8px;
    padding: 0px;
    margin-right:20px;
    /* display: inline-block; */
    width: 40%;
    text-align: center;
    background-color: red;
    color:white;
    outline:red;

}
.megamenu__column2 {
    display: flex;
    cursor: pointer;
    flex-direction: column;
    background-color: rgb(239, 244, 248);
    padding: 26px;
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
}
</style>