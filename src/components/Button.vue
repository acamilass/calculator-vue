<template>
    <button class="btn" 
        :class="{ double, triple, operation }" 
        @click="$emit('onClick', label)">
        {{ label }}
    </button>
</template>

<script>
export default {
    props: {
        label: {},
        operation: { type: Boolean },
        double: { type: Boolean },
        triple: { type: Boolean }
    }
}
</script>

<style>

:root {
    --bg-btn: #F0F0F0;
    --border-btn: solid 1px #888;
}

.btn {
    font-size: 1.4em;
    background-color: var(--bg-btn);
    border: none;
    border-right: var(--border-btn);
    border-bottom: var(--border-btn);
    outline: none;
}

.btn:active {
    background-color: #CCC;
}

.btn.double {
    grid-column: span 2;
}

.btn.triple {
    grid-column: span 3;
}

.btn.operation {
    background-color: #FA8231;
    color: #FFF;
}

.btn.operation:active {
    background-color: #FA8231cc;
}

</style>
