<template>
  <div class="browse-page">
    <div class="browse-header">
      <h1>Browse & Discover</h1>
      <p>Find the events and categories that matter most to you.</p>
    </div>
    <div class="browse-content">
      <router-view></router-view>
    </div>
  </div>
</template>

<style scoped>
.browse-page {
  animation: fadeIn 0.5s ease;
}

.browse-header {
  margin-bottom: 2.5rem;
}

.browse-header h1 {
  font-size: 2.2rem;
  color: #1c1948;
  margin-bottom: 0.5rem;
}

.browse-header p {
  color: #666;
  font-size: 1.05rem;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(10px); }
  to { opacity: 1; transform: translateY(0); }
}
</style>