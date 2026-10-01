<template>
  <div class="event-list-page">
    <div class="header-section">
      <h2 class="section-title">Upcoming Events</h2>
      <p class="section-desc">Discover the latest gatherings and activities happening near you.</p>
    </div>

    <div class="event-grid">
      <div class="event-card" v-for="i in 6" :key="i">
        <div class="event-body">
          <div class="event-meta">
            <span class="event-date">Oct {{ 10 + i }}, 2026</span>
            <span class="event-category">Community</span>
          </div>

          <h3>Community Gathering {{ i }}</h3>
          <p class="event-loc">📍 Main Auditorium, City Center</p>
          <p class="event-desc">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam at velit vel magna
            interdum scelerisque.
          </p>

          <div class="card-footer">
            <router-link :to="`/browse/events/${i}`" class="btn-link">
              View Details &rarr;
            </router-link>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.event-list-page {
  animation: fadeIn 0.5s ease;
}

.header-section {
  margin-bottom: 2rem;
}

.section-title {
  font-size: 1.8rem;
  color: #1c1948;
  margin-bottom: 0.5rem;
}

.section-desc {
  color: #666;
}

.event-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
  gap: 2rem;
}

.event-card {
  background: white;
  border-radius: 16px;
  border: 1px solid #f0f0f0;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.02);
  overflow: hidden;
  transition: all 0.3s ease;
}

.event-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.05);
}

.event-body {
  padding: 1.8rem;
}

.event-meta {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 1rem;
  font-size: 0.85rem;
}

.event-date {
  color: #6644ff;
  font-weight: 600;
}

.event-category {
  background: #f0ecff;
  color: #6644ff;
  padding: 0.2rem 0.8rem;
  border-radius: 20px;
  font-weight: 500;
}

.event-card h3 {
  color: #1c1948;
  font-size: 1.25rem;
  margin-bottom: 0.8rem;
}

.event-loc {
  color: #888;
  font-size: 0.9rem;
  margin-bottom: 1rem;
}

.event-desc {
  color: #666;
  font-size: 0.95rem;
  line-height: 1.6;
  margin-bottom: 1.5rem;
}

.card-footer {
  border-top: 1px solid #f5f5f5;
  padding-top: 1rem;
}

.btn-link {
  color: #6644ff;
  text-decoration: none;
  font-weight: 600;
  font-size: 0.95rem;
  transition: color 0.2s;
}

.btn-link:hover {
  color: #5533ee;
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>