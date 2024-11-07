<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
   <div id="app">
    <div class="d-flex" style="height: 100vh;">
      <!-- Sidebar -->
      <div class="bg-dark text-white p-3" style="width: 250px;" id="sidebar">
        <h4> Your Wallet</h4>
        <ul class="list-unstyled">
          <li><a href="#" class="text-white">Dashboard</a></li>
          <li><a href="#" class="text-white">Transactions</a></li>
          <li><a href="#" class="text-white">Budget</a></li>
        </ul>
      </div>
      
      <!-- Main content -->
      <div class="flex-grow-1 p-4">
        <nav class="navbar navbar-expand-lg navbar-light bg-light mb-4">
          <a class="navbar-brand" href="#"> YourWallet App</a>
          <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav ml-auto">
              <li class="nav-item active">
                <a class="nav-link" href="#">Welcome, User</a>
              </li>
            </ul>
          </div>
        </nav>

        <!-- Dashboard Widgets -->
        <div class="row">
          <!-- Total Balance Widget -->
          <div class="col-md-4 mb-3">
            <div class="card">
              <div class="card-body">
                <h5 class="card-title">Total Balance</h5>
                <p class="card-text">$12,345.67</p>
              </div>
            </div>
          </div>

          <!-- Recent Transactions Widget -->
          <div class="col-md-4 mb-3">
            <div class="card">
              <div class="card-body">
                <h5 class="card-title">Recent Transactions</h5>
                <ul>
                  <li>Payment to John: $100</li>
                  <li>Grocery shopping: $45</li>
                  <li>Salary: $2000</li>
                </ul>
              </div>
            </div>
          </div>

          <!-- Budget Widget -->
          <div class="col-md-4 mb-3">
            <div class="card">
              <div class="card-body">
                <h5 class="card-title">Budget Overview</h5>
                <p class="card-text">Remaining Budget: $500</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
body {
  font-family: Arial, sans-serif;
}

.sidebar {
  position: fixed;
  left: 0;
  bottom: 0;
  top: 0;
  z-index: 100;
  padding: 70px 0 0 10px;
  border-right: 1px solid #d3d3d3;
}
@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
