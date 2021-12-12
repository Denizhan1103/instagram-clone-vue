<template>
    <div class="header">
        <div class="container d-flex align-center justify-space">
            <img src="../assets/logo.png" alt="Instagram" class="header__logo">
            <input type="text" placeholder="Ara" class="header__search">
            <div class="header__navbar">
                <div v-for="x in 4" :key="x" class="header__navbar-item"></div>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import {Options,Vue} from "vue-class-component"

@Options({
    data() {
        return {
            Deneme: "Deneme"
        } 
    },
    methods: {
        changeDeneme():boolean {
            this.Deneme = 1
            return true
        }
    }
})

export default class Header extends Vue {

}

</script>

<style lang="scss" scoped>
@import "../styles/app.scss";
    .header {
        width: 100%;
        height: 60px;
        display: flex;
        justify-content: center;
        border-bottom: 1px solid #EAEAEA;
        margin-bottom: 30px;

        &__logo {
            width: 105px;
            height: 30px;
            object-fit: contain;
        }

        &__search {
            width: 270px;
            height: 36px;
            border: 1px solid #EAEAEA;
            color: #EAEAEA;
            padding: 0 20px;
            border-radius: 4px;

            &::placeholder {
                color: #B4B5B7;
            }
        }

        &__navbar {
            display: flex;
            align-items: center;
            justify-content: center;

            &-item {
                width: 24px;
                cursor: pointer;
                height: 24px;
                border-radius: 50%;
                background: #EAEAEA;
                margin-right: 20px;

                &:last-child {
                    margin-right: 0;
                }
            }
        }

    }
</style>