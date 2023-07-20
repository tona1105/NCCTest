<template>
    <div class="bg-sidebar">
        <ul>
            <li>Home</li>
            <li>Service</li>
            <li>News</li>
            <li>Blog</li>
            <li>Contact</li>
        </ul>
    </div>
</template>

<style>
.bg-sidebar {
    position: fixed;
    left: 0;
    top: 0;
    background-color: black;
    color: #e2f4f8;
    width: 10%;
    min-height: 100%;
}
ul {
    padding-left: 15px;
}
li {
    display: block;
    padding: 15px 0;
    position: relative;
}

li::after {
    content: '';
    position: absolute;
    width: calc(100% + 15px);
    bottom: 0;
    left: -15px;
    height: 1px;
    background-color: #252525;
}
</style>