<template>
    <div class="form-wrap">
        <div v-if="isShow" class="input-wrap">
            <input type="text" v-model="string" />
        </div>
        <div class="preview" @click="isShow = !isShow">{{string}}</div>
    </div>
</template>

<script setup>
import { ref, watch } from 'vue';

const string = ref('Edit me');
const isShow = ref(false);

</script>
<style>
.form-wrap {
    position: relative;
}
.input-wrap {
    background-color: #5c9bb7;
    background-image: -webkit-linear-gradient(top, #5c9bb7, #5392ad);
    background-image: -moz-linear-gradient(top, #5c9bb7, #5392ad);
    background-image: linear-gradient(top, #5c9bb7, #5392ad);
    box-shadow: 0 1px 1px #ccc;
    border-radius: 3px;
    width: 290px;
    padding: 10px;
    position: absolute;
    left: 50%;
    margin-left: -150px;
    top: -70px;
}
.input-wrap:after {
    content: '';
    position: absolute;
    border: 6px solid #5190ac;
    border-color: #5190ac transparent transparent;
    width: 0;
    height: 0;
    bottom: -12px;
    left: 50%;
    margin-left: -6px;
}
input {
    border: none;
    width: 100%;
    line-height: 34px;
    border-radius: 3px;
    box-shadow: 0 2px 6px #bbb inset;
    text-align: center;
    font-size: 16px;
    font-family: inherit;
    color: #8d9395;
    font-weight: bold;
    outline: none;
}
.preview {
    font-size: 22px;
    font-weight: bold;
    color: #6d8088;
    height: 30px;
    cursor: default;
}
</style>