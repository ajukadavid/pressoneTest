<template>
    <div>
        <div class="mobile-plans">
            <span class="main-title">Choose a plan that works for you</span>

            <marquee>
                <div class="wrapper">
                    <div class="plans">
                        <div>
                            <svg width="257" height="235" viewBox="0 0 257 235" fill="none"
                                xmlns="http://www.w3.org/2000/svg">
                                <path
                                    d="M127.92 161.117L70.0059 161.12L70.003 103.207C70.0046 103.176 70.0053 103.146 70.005 103.115C70.0037 102.952 70.003 102.788 70.003 102.624C70.0014 70.3171 96.1897 44.1262 128.496 44.1245C160.803 44.1229 186.994 70.3113 186.996 102.618C186.997 134.925 160.809 161.115 128.502 161.117C128.338 161.117 128.174 161.116 128.01 161.115C127.98 161.115 127.95 161.116 127.92 161.117ZM70.0065 173.719L99.6445 173.718L99.6454 190.877L70.0074 190.878L70.0065 173.719Z"
                                    fill="white" stroke="#87A7E6" stroke-width="3" stroke-linejoin="round" />
                                <path
                                    d="M83.4027 112.668C83.2533 110.944 82.731 106.216 87.7444 104.956C90.4586 104.273 93.9176 104.443 95.6927 106.861C97.4678 109.28 98.2546 111.649 96.1809 113.529C94.4026 115.14 92.3116 116.369 88.6787 116.773C85.8972 117.083 83.6257 115.243 83.4027 112.668Z"
                                    fill="#1BDE6C" />
                                <path
                                    d="M161.135 105.836C157.321 105.182 158.234 99.6294 161.801 97.011C163.736 95.5909 164.567 96.5703 167.689 95.7852C170.403 95.1027 171.865 98.5546 171.448 99.9326C170.881 101.806 171.014 104.246 168.999 104.707C166.053 105.382 165.902 106.653 161.135 105.836Z"
                                    fill="#FF3E13" />
                                <path
                                    d="M102.551 128.715L107.158 125.095C121.021 115.753 130.174 109.69 145.782 105.198C155.122 102.51 152.438 113.232 150.307 115.094C148.176 116.956 145.187 118.699 141.97 121.095C130.961 129.295 123.779 133.138 111.03 138.805C106.394 140.866 103.625 140.073 101.008 138.779C97.5185 137.053 98.4053 131.972 102.551 128.715Z"
                                    fill="#FFC20D" />
                                <path
                                    d="M106.225 94.4225L110.831 90.8027C124.694 81.4607 133.847 75.3978 149.455 70.9061C158.795 68.2183 156.111 78.9402 153.98 80.8022C151.849 82.6643 148.86 84.4065 145.643 86.8027C134.634 95.0029 127.452 98.8457 114.703 104.513C110.067 106.574 107.298 105.781 104.681 104.486C101.192 102.761 102.078 97.6802 106.225 94.4225Z"
                                    fill="#2D71F3" />
                            </svg>

                        </div>
                        <div class="plan-singular" v-for="plan in plans">
                            <span class="title">
                                {{ plan.name }}
                            </span>
                            <span class="pricing">
                                <span class="price">{{ plan.amount !== 'Custom' ?
                                    Number(plan.amount).toLocaleString('EN-us') : plan.amount }}</span><span
                                    v-if="plan.amount !== 'Custom'" class="date">/month</span>
                            </span>
                            <span class="desc">{{ plan.description }}</span>
                            <div class="button">
                                {{ plan.cta }}
                            </div>
                        </div>
                    </div>
                    <div class="table">
                        <table>
                            <tbody>
                                <tr class="top">
                                    <td>
                                        <div class="table-title">
                                            <span>Call reception</span>
                                        </div>

                                    </td>
                                    <td v-for="plan in plans">
                                        <div class="items" :class="{ 'last-item': plan.id === 3 }">
                                            <span>
                                                {{ plan.call_reception }}
                                            </span>
                                        </div>

                                    </td>

                                </tr>
                                <tr class="middle">
                                    <td>
                                        <div class="table-title">
                                            <span> Calls per week </span>
                                        </div>
                                    </td>

                                    <td v-for="plan in plans">
                                        <div class="items" :class="{ 'last-item': plan.id === 3 }">
                                            <span>
                                                {{ plan.calls_per_week }}
                                            </span>
                                        </div>

                                    </td>

                                </tr>
                                <tr class="bottom">
                                    <td>
                                        <div class="table-title">
                                            <span>Agents</span>
                                        </div>
                                    </td>
                                    <td class="last" v-for="plan in plans">
                                        <div class="items" :class="{ 'last-item': plan.id === 3 }">
                                            <span>
                                                {{ plan.agent }}

                                            </span>
                                        </div>


                                    </td>

                                </tr>
                            </tbody>
                        </table>
                    </div>
                </div>

            </marquee>
            <div class="banner">
                <span class="banner-title">
                    Join thousands of entrepreneurs using PressOne to improve their business communications.
                </span>
                <span class="banner-sub">
                    Ready to make your customers love your business?
                </span>
                <div class="banner-button">
                    Join Now
                </div>
            </div>
        </div>
        <div class="desktop-plans">
            <span class="main-title">Choose a plan that works for you</span>

            <div class="wrapper">
                <div class="plans">
                    <div>
                        <svg width="257" height="235" viewBox="0 0 257 235" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path
                                d="M127.92 161.117L70.0059 161.12L70.003 103.207C70.0046 103.176 70.0053 103.146 70.005 103.115C70.0037 102.952 70.003 102.788 70.003 102.624C70.0014 70.3171 96.1897 44.1262 128.496 44.1245C160.803 44.1229 186.994 70.3113 186.996 102.618C186.997 134.925 160.809 161.115 128.502 161.117C128.338 161.117 128.174 161.116 128.01 161.115C127.98 161.115 127.95 161.116 127.92 161.117ZM70.0065 173.719L99.6445 173.718L99.6454 190.877L70.0074 190.878L70.0065 173.719Z"
                                fill="white" stroke="#87A7E6" stroke-width="3" stroke-linejoin="round" />
                            <path
                                d="M83.4027 112.668C83.2533 110.944 82.731 106.216 87.7444 104.956C90.4586 104.273 93.9176 104.443 95.6927 106.861C97.4678 109.28 98.2546 111.649 96.1809 113.529C94.4026 115.14 92.3116 116.369 88.6787 116.773C85.8972 117.083 83.6257 115.243 83.4027 112.668Z"
                                fill="#1BDE6C" />
                            <path
                                d="M161.135 105.836C157.321 105.182 158.234 99.6294 161.801 97.011C163.736 95.5909 164.567 96.5703 167.689 95.7852C170.403 95.1027 171.865 98.5546 171.448 99.9326C170.881 101.806 171.014 104.246 168.999 104.707C166.053 105.382 165.902 106.653 161.135 105.836Z"
                                fill="#FF3E13" />
                            <path
                                d="M102.551 128.715L107.158 125.095C121.021 115.753 130.174 109.69 145.782 105.198C155.122 102.51 152.438 113.232 150.307 115.094C148.176 116.956 145.187 118.699 141.97 121.095C130.961 129.295 123.779 133.138 111.03 138.805C106.394 140.866 103.625 140.073 101.008 138.779C97.5185 137.053 98.4053 131.972 102.551 128.715Z"
                                fill="#FFC20D" />
                            <path
                                d="M106.225 94.4225L110.831 90.8027C124.694 81.4607 133.847 75.3978 149.455 70.9061C158.795 68.2183 156.111 78.9402 153.98 80.8022C151.849 82.6643 148.86 84.4065 145.643 86.8027C134.634 95.0029 127.452 98.8457 114.703 104.513C110.067 106.574 107.298 105.781 104.681 104.486C101.192 102.761 102.078 97.6802 106.225 94.4225Z"
                                fill="#2D71F3" />
                        </svg>

                    </div>
                    <div class="plan-singular" v-for="plan in plans">
                        <span class="title">
                            {{ plan.name }}
                        </span>
                        <span class="pricing">
                            <span class="price">{{ plan.amount !== 'Custom' ?
                                Number(plan.amount).toLocaleString('EN-us') : plan.amount }}</span><span
                                v-if="plan.amount !== 'Custom'" class="date">/month</span>
                        </span>
                        <span class="desc">{{ plan.description }}</span>
                        <div class="button">
                            {{ plan.cta }}
                        </div>
                    </div>
                </div>
                <div class="table">
                    <table>
                        <tbody>
                            <tr class="top">
                                <td>
                                    <div class="table-title">
                                        <span>Call reception</span>
                                    </div>

                                </td>
                                <td v-for="plan in plans">
                                    <div class="items" :class="{ 'last-item': plan.id === 3 }">
                                        <span>
                                            {{ plan.call_reception }}
                                        </span>
                                    </div>

                                </td>

                            </tr>
                            <tr class="middle">
                                <td>
                                    <div class="table-title">
                                        <span> Calls per week </span>
                                    </div>
                                </td>

                                <td v-for="plan in plans">
                                    <div class="items" :class="{ 'last-item': plan.id === 3 }">
                                        <span>
                                            {{ plan.calls_per_week }}
                                        </span>
                                    </div>

                                </td>

                            </tr>
                            <tr class="bottom">
                                <td>
                                    <div class="table-title">
                                        <span>Agents</span>
                                    </div>
                                </td>
                                <td class="last" v-for="plan in plans">
                                    <div class="items" :class="{ 'last-item': plan.id === 3 }">
                                        <span>
                                            {{ plan.agent }}

                                        </span>
                                    </div>


                                </td>

                            </tr>
                        </tbody>
                    </table>
                </div>
            </div>

            <div class="banner">
                <span class="banner-title">
                    Join thousands of entrepreneurs using PressOne to improve their business communications.
                </span>
                <span class="banner-sub">
                    Ready to make your customers love your business?
                </span>
                <div class="banner-button">
                    Join Now
                </div>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
import { onMounted, ref } from 'vue';


const plans = ref<any>([])
async function getData() {
    const response = await fetch("/data.json");
    const data = await response.json();
    plans.value = data.data
}


onMounted(() => {
    getData()
})
</script>

<style scoped>
.mobile-plans {
    display: none;
}

.items {
    padding-left: 10px;
}

tr:nth-child(odd) {
    background-color: #EAF1F6;
}

.banner-title {
    font-family: 'Recoleta', sans-serif;
    font-size: 32px;
    font-weight: 600;
    color: white;
    line-height: 52px;
    letter-spacing: 0em;
    text-align: center;

}

.main-title {
    font-family: 'Recoleta', sans-serif;
    font-size: 40px;
    font-weight: 600;
    line-height: 52px;
    letter-spacing: 0em;

    margin-bottom: 40px;
    text-align: center;
}

.plans {
    display: flex;
}

.banner-sub {
    font-family: 'Urbanist', sans-serif;
    font-size: 20px;
    color: white;
    font-weight: 500;
    line-height: 26px;
    letter-spacing: 0em;
    margin-top: 9px;
    text-align: center;

}

.banner {
    display: flex;
    margin-top: 20px;
    padding: 30px;
    margin-inline: 40px;
    flex-direction: column;
    align-items: center;
    background: url('/join_cleanup.png');
    height: fit-content;
    background-repeat: no-repeat;
    background-position: center center;
    background-size: cover;
    border-top-left-radius: 3% 3%;
    border-top-right-radius: 3% 3%;
}

.table-title {
    padding-left: 20px;
    padding-block: 20px;
}

.last-item {
    padding-left: 30px;
}

.table {
    margin-top: 32px;
    font-size: 12px;
    margin-bottom: 120px;
}



.pricing {
    margin-bottom: 8px;
}

td {
    width: 314px;

}



.banner-button {
    background: white;
    color: #0E99D2;
    display: flex;
    border: 1px solid #0E99D2;
    border-radius: 4px;
    justify-content: center;
    cursor: pointer;
    align-items: center;
    width: 266px;
    height: 47px;
    margin-top: 40px;
}

.desc {
    font-family: 'Urbanist', sans-serif;
    font-size: 16px;
    font-weight: 500;
    line-height: 21px;
    letter-spacing: 0em;
    color: #616C74;

}

.price {
    font-size: 32px;
    font-family: 'Recoleta', sans-serif;
    line-height: 41.6px;
    font-weight: 600;
    color: #212121;
}

.date {
    font-family: 'Urbanist', sans-serif;
    font-size: 14px;
    font-weight: 500;
    color: #A7B4BE;
    line-height: 20px;
    letter-spacing: 0em;
    text-align: center;


}

.plan-singular {
    padding-top: 12px;
    display: flex;
    margin-right: 24px;
}

.plan-singular>.title {
    font-family: 'Urbanist', sans-serif;
    font-size: 16px;
    font-weight: 700;
    line-height: 21px;
    color: #0E99D2;
    margin-block: 8px;
    letter-spacing: 0em;

}

.desktop-plans {
    display: flex;
    flex-direction: column;
    margin-top: 50px;
}

.plan-singular {
    display: flex;
    flex-direction: column;
    box-shadow: 1px 1px 5px lightgray;
    width: 200px;
    padding-left: 20px;
    border: 1px solid lightgray;
    border-radius: 12px;
    height: 235px;
}

.button {
    background: #0E99D2;
    color: white;
    display: flex;
    justify-content: center;
    cursor: pointer;
    align-items: center;
    width: fit-content;
    padding-inline: 12px;
    height: 47px;
    margin-top: 40px;
}

@media (max-width: 768px) {
    .mobile-plans {
        display: block;
    }

    .button {
        background: #0E99D2;
        color: white;
        display: flex;
        justify-content: center;
        cursor: pointer;
        align-items: center;
        width: 266px;
        height: 47px;
        margin-top: 40px;
    }

    .desktop-plans {
        display: none;
    }

    .banner {
        display: flex;
        margin-top: 20px;
        padding: 10px;
        margin-inline: 40px;
        flex-direction: column;
        align-items: center;
        background: url('/join_cleanup.png');
        height: fit-content;
        background-repeat: no-repeat;
        background-position: center center;
        background-size: cover;
        border-top-left-radius: 3% 3%;
        border-top-right-radius: 3% 3%;
    }

    .plans {
        display: flex;
        gap: 24px;
    }

    .wrapper {
        display: grid;

    }

    .plan-singular {
        display: flex;
        flex-direction: column;
        box-shadow: 1px 1px 5px lightgray;
        width: 314px;
        padding-left: 20px;
        border: 1px solid lightgray;
        border-radius: 12px;
        height: 235px;
    }
}
</style>