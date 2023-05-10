<script setup lang="ts">
import Button from '../components/Button.vue';
import Image from '../components/Image.vue';
import Slider from '../components/Slider.vue';
import Textarea from '../components/Textarea.vue';
</script>

<template>
    <section id="home">

        <!-- Generated image -->
        <section id="home-img">
            <Image src="" size="16em" />
        </section>

        <!-- Generation form -->
        <section id="home-form">
            <h2>Generate an image!</h2>
            <form action="">
                <ul>
                    <li>
                        <Textarea label="Prompt" placeholder="Something interesting" required />
                    </li>
                    <li>
                        <Slider label="Steps" :min=1 :max=10 />
                    </li>
                    <li>
                        <Button label="Generate" required />
                    </li>
                </ul>
            </form>
        </section>
    </section>
</template>

<style scoped lang="scss">
section#home {
    display: flex;
    flex-direction: column;
    gap: 1.2rem 0;
    padding: 2em;

    section#home-form {
        background: #f2f2f2;
        border-radius: 4px;
        box-shadow: rgba(0, 0, 0, 0.16) 0px 1px 4px;
        padding: 1.8em 1.4em;

        >h2 {
            color: #01a2a6;
            font-size: 1.2em;
            margin: 0 0 1rem;
        }

        >form>ul {
            display: flex;
            flex-direction: column;
            gap: .8rem 0;
            list-style-type: none;
            margin: 0;
            padding: 0;
        }
    }
}

@media only screen and (min-device-width: 768px) {

    section#home {
        align-items: center;
        flex-direction: row-reverse;
        gap: 0 2rem;
    }
}
</style>
