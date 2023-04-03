<script setup>
</script>
<template>
    <div class="menubar__megamenu megamenu">
        <div class="flex justify-center gap-5 ">

            <div class="megamenu__column1">
                <h4>home page1</h4>
                <div>home1</div>
                <div>home2</div>
                <div>home3</div>
                <div>home4</div>
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
            <div class="megamenu__column2 sale ">
                <div class="flex justify-center gap-5">
                    <h5>sale collection</h5>
                    <div>
                        <p>up to 80% off retail</p>
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
    height: 300px;
    background-color: white;
    top: 0;
    margin-top: 100px;
    transform: scale(1, 0);
    transition: transform 100ms ease-in-out;
    z-index: 2;
    box-shadow: 0 4px 6px -1px rgb(0 0 0 / 0.1), 0 2px 4px -2px rgb(0 0 0 / 0.1);
}

.megamenu__column1 {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-left: 3rem;
    cursor: pointer
}
.megamenu__column2 {
    display: flex;
    flex-direction: column;

}
</style>