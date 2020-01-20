<template>
  <nav class="navbar navbar-default">
    <div class="container-fluid">
      <div class="navbar-header">
        <router-link to="/" class="navbar-brand">Stock Trader</router-link>
      </div>
      <ul class="nav navbar-nav">
        <router-link to="/portfolio" activeClass="active" tag="li">
          <a>Portfolio</a>
        </router-link>
        <router-link to="/stocks" activeClass="active" tag="li">
          <a>Stocks</a>
        </router-link>

        <li>
          <a href="#">Page 2</a>
        </li>
        <li>
          <a href="#">Page 3</a>
        </li>
      </ul>
    </div>
  </nav>
</template>