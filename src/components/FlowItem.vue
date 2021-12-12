<template>
    <div class="flowitem">
        <div class="flowitem__title">
            <div class="flowitem__title-image"></div>
            <div class="flowitem__title-name">Denizhan Onur</div>
            <div class="flowitem__title-options">...</div>
        </div>
        <img src="https://www.hobisi.com/wp-content/uploads/2019/05/resim-nedir-turleri-ve-stilleri.jpg" alt="" class="flowitem__image">
        <div class="flowitem__navbar">
            <div v-for="x in 5" :key="x" class="flowitem__navbar-item"></div>
        </div>
        <div class="flowitem__footer">
            <div class="flowitem__footer-like"><span>2.204</span> Beğenme</div>
            <div class="flowitem__footer-description">
                <span>Denizhan Onur</span>
                Tanıdık Geldi
            </div>
            <div class="flowitem__footer-comments">49 yorumun tümünü gör</div>
            <div class="flowitem__footer-time">5 Saat Önce</div>
        </div>
        <div class="flowitem__comment">
            <div class="flowitem__comment-image"></div>
            <input type="text" placeholder="Yorum Ekle..." class="flowitem__comment-input">
            <button class="flowitem__comment-share">Paylaş</button>
        </div>
    </div>
</template>

<script lang="ts">
import {Options,Vue} from "vue-class-component"

@Options({
    data() {
        return {

        }
    }
})

export default class FlowItem extends Vue{}
</script>

<style lang="scss" scoped>
    .flowitem {
        width: 615px;
        border: 1px solid #EAEAEA;
        border-radius: 2px;
        margin-bottom: 30px;
        
        &__title {
            display: flex;
            padding: 0 20px;
            height: 60px;
            align-items: center;

            &-image {
                border-radius: 50%;
                width: 36px;
                background: #EAEAEA;
                height: 36px;
                margin-right: 20px;
            }

            &-name {
                flex: 1;
                text-align: start;
                color: #262626;
                font-weight: bold;
                font-size: 14px;
            }

            &-options {
                font-weight: bold;
                color: #262626;
                letter-spacing: 2px;
                cursor: pointer;
                height: 28px;
            }
        }

        &__image {
            width: 100%;
            max-height: 614px;
            margin-bottom: 10px;
            object-fit: contain;
        }

        &__navbar {
            width: 100%;
            padding: 0 20px;
            display: flex;
            margin-bottom: 10px;

            &-item {
                margin-right: 10px;
                width: 28px;
                height: 28px;
                background: #EAEAEA;
                border-radius: 50%;

                &:nth-child(4) {
                    border-radius: 0;
                    background: none;
                    flex: 1;
                }

                &:last-child {
                    margin-right: 0;
                }
            }
        }

        &__footer {
            width: 100%;
            padding: 0 20px;
            text-align: start;
            margin-bottom: 20px;

            &-like,
            &-description,
            &-comments,
            &-time {
                font-size: 14px;
                margin-bottom: 5px;

                span {
                    font-weight: 600;
                }
            }

            &-time {
                font-size: 12px;
            }

        }

        &__comment {
            height: 50px;
            padding: 0 20px;
            display: flex;
            align-items: center;
            border-top: 1px solid #EAEAEA;

            &-image {
                width: 28px;
                height: 28px;
                border-radius: 50%;
                background: #EAEAEA;
                margin-right: 20px;
            }

            &-input {
                flex: 1;
            }

            &-share {
                color: #0095f6;
                opacity: 0.3;
                font-weight: 600;
                cursor: pointer;
            }
        }
    }
</style>