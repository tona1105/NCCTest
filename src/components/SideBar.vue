<template>
    <div class="bg-sidebar">
        <ul>
            <li style="font-weight: bold;">Home</li>
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
    z-index: 1000;
}
ul {
    margin: 0;
    padding: 0;
}
li {
    
    display: block;
    padding: 15px 0 15px 15px;
    position: relative;
}

li:hover {
    background-color: #5C5C5C;
    font-weight: bold;
    overflow: hidden;
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