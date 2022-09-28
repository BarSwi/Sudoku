<template>
    <div id="area-home-animation">
        <li>1</li>
        <li>2</li>
        <li>3</li>
        <li>4</li>
        <li>5</li>
        <li>6</li>
        <li>7</li>
        <li>8</li>
        <li>9</li>
        <svg id = 'test' stroke = 'red' viewBox = "0 0 297 297">

        </svg>
    </div>


</template>
<style lang = 'scss'>
    #area-home-animation{
        height: 100vh;
        width: 100%;
        position: relative;
        overflow: hidden;
        background: linear-gradient(to top, #FFA303, #A2ABCE 45%);
        -webkit-background:  linear-gradient(to right, #03045e, #023e8a);

        li{
            position: absolute;
            display: block;
            list-style: none;
            width: 150px;
            color: #FF4A38;
            height: 150px;
            -webkit-user-select: none; 
            -ms-user-select: none; 
            user-select: none; 
            text-align: center;
            font-weight: 900;
            font-size: 75px;
            line-height: 150px;
            background: #FFE0AE;
            animation: animate 25s linear infinite;
            top: -150px;
        }
        li:nth-child(1){
            left: 15%;  
            animation-delay: var(--animation-delay);
            animation-duration: 13s;
        }
        li:nth-child(2){
            left: 25%;  
            animation-delay: 2s;
            animation-duration: 17s;
            animation-delay: var(--animation-delay);
        }
        li:nth-child(3){
            left: 35%;  
            animation-delay: 5s;
            animation-delay: var(--animation-delay);
            animation-duration: 14s;
        }
        li:nth-child(4){
            left: 45%;  
            animation-delay: 0s;
            animation-duration: 15s;
            animation-delay: var(--animation-delay);
        }
        li:nth-child(5){
            left: 55%;  
            animation-delay: 3s;
            animation-delay: var(--animation-delay);
            animation-duration: 16s;
        }
        li:nth-child(6){
            left: 65%;  
            animation-delay: 7s;
            animation-delay: var(--animation-delay);
            animation-duration: 19s;
        }
        li:nth-child(7){
            left: 75%;  
            animation-delay: 15s;
            animation-duration: 25s;
            animation-delay: var(--animation-delay);
        }
        li:nth-child(8){
            left: 85%;  
            animation-delay: 8s;
            animation-duration: 10s;
            animation-delay: var(--animation-delay);
        }
        li:nth-child(9){
            left: 95%;  
            animation-delay: 9s;
            animation-duration: 18s;
            animation-delay: var(--animation-delay);
        }
        #test{
            height: 250px;
            width: 250px;
            z-index: 5;
        }




        @keyframes animate {

        0%{
            transform: translateY(0) rotate(0deg);
            opacity: 1;
            border-radius: 0;
        }

        100%{
            transform: translateY(110vh) rotate(720deg);
            opacity: 0;
            border-radius: 40%;
        }

        }
    }
    
</style>
<script>
    export default {
        methods: {
            randomAnimationDelay(){
                let li = document.getElementById('area-home-animation').getElementsByTagName('li');
                for(let el of li){
                    let time = Math.ceil(Math.random() * 15);
                    el.style.setProperty('--animation-delay', time + 's')
                }
            }
        },
        mounted(){
                this.randomAnimationDelay();  
            }
    }
</script>