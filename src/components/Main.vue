<script lang="ts" setup>
</script>

<template>
    <div class="summary-wrapper">
        <div class="card-wrapper">
            <div class="card-circle">
                <div class="inner">

                </div>
            </div>
            <div class="card-square">
                <div class="inner">

                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.summary-wrapper {
    background: #0E99D2;
    border: 1px solid #0E99D2;
    border-radius: 40px;
    margin-top: 40px;
    display: flex;
    padding-block: 20px;
    align-items: center;
    justify-items: center;
}

.card-wrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.card-circle {
    width: 100px;
    height: 100px;
    padding: 10px;
    background-color: white;
    border-radius: 50%;
    position: relative;
    top: 50px;
}

.card-square {
    width: 294px;
    height: 200px;
    background-color: white;
    border-radius: 12px;
    padding: 10px;
}

.card-square>.inner {
    width: inherit;
    height: inherit;
    background: #F3F8FE;
    border-radius: 12px;
}

.card-circle>.inner {
    width: 100px;
    height: 100px;
    background: #F3F8FE;
    border-radius: 50%;
}

@media (max-width: 768px) {}
</style>