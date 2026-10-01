<script setup>
import { useRoute } from 'vue-router'

const route = useRoute()
</script>

<template>
  <div class="event-detail-page">
    <button @click="$router.push('/browse/events')" class="btn-back">&larr; Back to Events</button>

    <div class="detail-header">
      <div class="header-content">
        <span class="event-tag">Community Event</span>
        <h1>Community Gathering {{ route.params.id }}</h1>
        <div class="meta-info">
          <div class="meta-item">
            <span class="icon">📅</span>
            <span>October 15, 2026</span>
          </div>
          <div class="meta-item">
            <span class="icon">📍</span>
            <span>Main Auditorium, City Center</span>
          </div>
          <div class="meta-item">
            <span class="icon">👥</span>
            <span>500+ Attendees</span>
          </div>
        </div>
      </div>
    </div>

    <div class="detail-content">
      <div class="main-desc">
        <h2>About This Event</h2>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam in dui mauris. Vivamus hendrerit arcu
          sed erat molestie vehicula. Sed auctor neque eu tellus rhoncus ut eleifend nibh porttitor. Ut in
          nulla enim. Phasellus molestie magna non est bibendum non venenatis nisl tempor.
        </p>
        <p>
          Suspendisse dictum feugiat nisl ut dapibus. Mauris iaculis porttitor posuere. Praesent id
          metus massa, ut blandit odio. Proin quis tortor orci. Etiam at risus et justo dignissim
          congue. Donec congue lacinia dui, a porttitor lectus condimentum laoreet. Nunc eu ullamcorper orci.
        </p>

        <h2>Agenda</h2>
        <ul class="agenda-list">
          <li><strong>09:00 AM</strong> - Registration & Welcome Coffee</li>
          <li><strong>10:00 AM</strong> - Opening Keynote Speech</li>
          <li><strong>11:30 AM</strong> - Networking Session</li>
          <li><strong>01:00 PM</strong> - Closing Remarks</li>
        </ul>
      </div>

      <div class="sidebar">
        <div class="ticket-card">
          <h3>Registration</h3>
          <p class="price">Free</p>
          <p class="ticket-desc">Secure your spot today before it runs out.</p>
          <button class="btn-register">Register Now</button>
          <p class="spots">Only 45 spots left!</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.event-detail-page {
  animation: fadeIn 0.5s ease;
}

.btn-back {
  background: none;
  border: none;
  color: #6644ff;
  font-weight: 600;
  font-size: 0.95rem;
  cursor: pointer;
  margin-bottom: 2rem;
  padding: 0;
  transition: transform 0.2s;
}

.btn-back:hover {
  transform: translateX(-5px);
}

.detail-header {
  background: linear-gradient(135deg, #1c1948 0%, #2a2566 100%);
  color: white;
  padding: 3rem;
  border-radius: 20px;
  margin-bottom: 2.5rem;
}

.event-tag {
  background: rgba(255, 255, 255, 0.15);
  padding: 0.3rem 1rem;
  border-radius: 20px;
  font-size: 0.85rem;
  font-weight: 500;
  display: inline-block;
  margin-bottom: 1rem;
}

.detail-header h1 {
  font-size: 2.5rem;
  margin-bottom: 1.5rem;
}

.meta-info {
  display: flex;
  gap: 2rem;
  flex-wrap: wrap;
}

.meta-item {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  font-size: 0.95rem;
  opacity: 0.9;
}

.detail-content {
  display: grid;
  grid-template-columns: 2fr 1fr;
  gap: 3rem;
}

.main-desc h2 {
  color: #1c1948;
  font-size: 1.5rem;
  margin-top: 2rem;
  margin-bottom: 1rem;
}

.main-desc h2:first-child {
  margin-top: 0;
}

.main-desc p {
  color: #555;
  line-height: 1.8;
  margin-bottom: 1.5rem;
}

.agenda-list {
  list-style: none;
  padding: 0;
}

.agenda-list li {
  padding: 1rem 0;
  border-bottom: 1px solid #eee;
  color: #555;
}

.ticket-card {
  background: white;
  padding: 2rem;
  border-radius: 16px;
  border: 1px solid #f0f0f0;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
  position: sticky;
  top: 100px;
}

.ticket-card h3 {
  color: #1c1948;
  margin-bottom: 0.5rem;
}

.price {
  font-size: 2rem;
  font-weight: 700;
  color: #6644ff;
  margin-bottom: 1rem;
}

.ticket-desc {
  color: #666;
  font-size: 0.9rem;
  margin-bottom: 1.5rem;
}

.btn-register {
  width: 100%;
  padding: 1rem;
  background: #6644ff;
  color: white;
  border: none;
  border-radius: 10px;
  font-weight: 600;
  font-size: 1rem;
  cursor: pointer;
  transition: background 0.3s;
  margin-bottom: 1rem;
}

.btn-register:hover {
  background: #5533ee;
}

.spots {
  color: #e53e3e;
  font-size: 0.85rem;
  text-align: center;
  font-weight: 500;
}

@media (max-width: 768px) {
  .detail-content {
    grid-template-columns: 1fr;
  }
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