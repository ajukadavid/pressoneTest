<script setup lang="ts">

</script>

<template>
    <div class="hero-wrapper">
        <div class="hero">
            <div class="hero-text">
                <span class="hero-title">You do the work, <br /> We'll do the talk</span>
                <span class="hero-subText">Move your customers' <span>enquiry</span> to our <br /> team of experts</span>
                <span class="hero-summary">Let us manage your customer relationship from their first call till they become
                    your raving
                    fans</span>
                <div class="button">
                    Get started
                </div>
            </div>
            <div class="hero-img">
                <img src="/hero-img.png" />
            </div>
        </div>
    </div>
</template>

<style scoped>
@import url('https://fonts.cdnfonts.com/css/recoleta');
@import url('https://fonts.googleapis.com/css2?family=Urbanist&display=swap');

.hero-wrapper {
    padding-inline: 50px;
    margin-top: 74px;
}

.hero-title {
    font-size: 48px;
    font-family: 'Recoleta', sans-serif;
    color: #212121;
    font-weight: 600;
    line-height: 62.4px;
}

.hero-img {
    background-image: url('hero-img-bg.png');
    background-repeat: no-repeat;
    background-position: center center;
    background-size: cover;
}

.hero {
    display: flex;
    align-items: center;

}

.hero-subText {
    font-size: 32px;
    margin-top: 32px;
    font-weight: 700;
    font-family: 'Recoleta', sans-serif;
    color: #212121;
    line-height: 41.6px;

}

.hero-subText>span {
    color: #0E99D2;
}

.hero-summary {
    font-family: 'Urbanist', sans-serif;
    margin-top: 16px;
    font-weight: 100;
    margin-bottom: 64px;
}

.hero-text {
    display: flex;
    margin-top: 30px;
    background-image: url('hero-text-bg.png');
    background-repeat: no-repeat;
    background-position: center center;
    background-size: cover;
    flex-direction: column;
}

.button {
    background: #0E99D2;
    color: white;
    display: flex;
    justify-content: center;
    cursor: pointer;
    align-items: center;
    width: 320px;
    padding-block: 17px;
}


@media (max-width: 768px) {
    .hero-wrapper {
        padding-inline: 34px;
        margin-top: 20px;
    }

    .hero {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .hero-title {
        font-size: 36px;
        text-align: center;
        line-height: 45px;
    }

    .hero-img {
        height: 300px;

    }

    .hero-img>img {
        height: auto;
        width: 100%;

    }

    .hero-subText {
        font-size: 24px;
        margin-top: 16px;
        text-align: center;
        line-height: 25px;

    }

    .hero-summary {
        margin-bottom: 16px;
        text-align: center;
    }

    .hero-text {
        padding: 10px;
        display: flex;
        flex-direction: column;
        margin-bottom: 30px;
    }

    .button {
        width: 100%;
        font-size: 18px;
        padding-block: 12px;
    }
}
</style>
