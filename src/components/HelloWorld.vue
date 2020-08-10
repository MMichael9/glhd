<template>
    <div class="hello">
        <h1>{{ msg }}</h1>
        <p>
            WE ARE NOW REOPENED!<br />
            Please ensure that you bring your own mask upon arrival. For more
            guildines and protocols, please click
            <a
                href="https://www.worksafebc.com/en/about-us/covid-19-updates/covid-19-returning-safe-operation/personal-services"
                target="_blank"
                rel="noopener"
                >here</a
            >.
        </p>
        <h3>Contact Us</h3>
        <p>
            1201 Ewen Ave #130 <br />
            New Westminster, BC <br />
            V3M 5E5 <br />
            Phone: 604-525-2442
        </p>
        <h3>Hours</h3>
        <p>
            Monday: 11am -6pm <br />
            Tuesday: Closed<br />
            Wednesday: 10am -6pm<br />
            Thursday: 10am -6pm<br />
            Friday: 10am -6pm<br />
            Saturday: 10am -6pm<br />
            Sunday: 11am -5pm
        </p>

        <p>
            If you enjoyed our services today, please leave us a review
            <a
                href="https://www.google.com/search?gs_ssp=eJzj4tZP1zcsSSk0Lag0MmC0UjWoMDWxME2xsDQzt7C0MDRMsrQyqDA3TzYwTzO0MDGzNLM0N0r0Ek3Pz09RyMnPz1bISMwsUkhJLc5MzwMAAfMVmw&q=good+look+hair+design&oq=good+&aqs=chrome.2.69i59l2j46j69i57j69i60l4.2733j0j9&sourceid=chrome&ie=UTF-8#lrd=0x5485d896789811b9:0x77c07f184696972a,1,,,"
                target="_blank"
                rel="noopener"
                >here</a
            >.
        </p>
    </div>
</template>

<script>
export default {
    name: 'HelloWorld',
    props: {
        msg: String
    }
};
</script>

<style scoped></style>
