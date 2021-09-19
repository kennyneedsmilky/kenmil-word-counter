<template>
    <div class="word-counter">
      <h2>Word Counter</h2>
      <form>
          <textarea class="word-counter__txtarea" v-model="msg" placeholder="Write or paste something here."></textarea>
      </form>
      <p v-if="this.msg === ''" class="word-counter__count-label">Word Count: 0</p>
      <p v-else class="word-counter__count-label --blue">Word Count: {{ numberCounter }}</p>
    </div>
</template>

<script>
export default {
    name: "WordCounter",
    data() {
        return {
            msg: "",
        }
    },
    computed: {
        numberCounter: function() {
            return this.msg.trim().split(/\s+/).length;
        }
    }
}
</script>

<style scoped>
    .word-counter {
        padding: 0.25rem;
        border-radius: 0.25rem;
        background-color: #3c394ef0;
        box-shadow: 5px 5px 5px #00000080;
        margin: 0.25rem;
        width: calc(100% - 1rem);
        max-width: 800px;
        color: #f5f5f5;
        transition: 0.25s;
    }

    .word-counter:hover, .word-counter:active {
        background-color: #000000;
    }

    .word-counter__txtarea {
        outline: none;
        padding: 0.5rem;
        border: 0.25rem  solid #f5f5f5;
        border-radius: 0.25rem;
        background-color: #000000;
        margin: 0;
        width: calc(100% - 1.5rem);
        height: 50vh;
        resize: none;
        font-size: 1.5rem;
        color: #f5f5f5;
        transition: 0.25s;
    }

    .word-counter__txtarea:focus {
       border: 0.25rem  solid #00ffea;
       background-color: #17161f;
    }

    .word-counter__count-label {
        text-align: right;
        font-size: 1.25rem;
        font-weight: bold;
    }

    .word-counter__count-label.--blue {
        color: #00ffea;
    }
</style>