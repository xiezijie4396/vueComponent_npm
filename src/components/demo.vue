<template>
    <div class="test">
        <div class="box">
            <div class="header">{{ header }}</div>
            <div class="body" @click="testClick">点击事件在此</div>
            <div class="footer">{{ clickNum }}</div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'demo',
    data() {
        return {
            header: "这是来自data的header",
            num: 0,
        };
    },
    computed: {
        clickNum() {
            return `点击次数${this.num}`;
        },
    },
    methods: {
        testClick() {
            this.num++;
        },
    },
};
</script>

<style>
.test {
    width: 100vw;
    height: 100vh;
    position: relative;
    background: rgba(0, 0, 0, 0.5);
}
.box {
    width: 200px;
    height: 200px;
    display: flex;
    flex-direction: column;
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
}
.header,
.body,
.footer {
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    color: #fff;
}
.header {
    flex-basis: 20%;
    background: darkblue;
}
.body {
    flex-basis: 60%;
    background: darkcyan;
}
.footer {
    flex-basis: 20%;
    background: darkorange;
}
</style>
