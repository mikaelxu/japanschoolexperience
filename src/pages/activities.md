---
title: Activities
permalink: /activities/index.html
description: 'Discover the exciting leisure activities available during your Japan School Experience program.'
layout: page
---

# Leisure Activities

During your Japan School Experience program, you'll have the opportunity to participate in a variety of authentic Japanese leisure activities. 

We have carefully selected the following 5 activities to immerse you in local culture and provide memorable experiences beyond the classroom.

<style>
.activity-image-container {
  position: relative;
  overflow: hidden;
  border-radius: 8px;
}

.activity-image-container::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(0, 0, 0, 0);
  transition: background 0.3s ease;
  z-index: 1;
  pointer-events: none;
}

.activity-image-container:hover::before {
  background: rgba(0, 0, 0, 0.5);
}

.activity-image-container img {
  width: 100%;
  height: auto;
  border-radius: 8px;
  transition: transform 0.3s ease;
  display: block;
  cursor: pointer;
  position: relative;
  z-index: 2;
}

.activity-image-container:hover img {
  transform: scale(1.05);
}
</style>

## Available Activities

### 🚗 Aso Drive
Explore the beautiful Aso region with a scenic drive through one of Japan's most stunning volcanic landscapes. Discover the natural beauty and cultural sites of this unique area. [Download Aso Drive Map (PDF)](/assets/PDFs/AsoDriveMap.pdf){target="_blank" rel="noopener noreferrer"}

<div class="grid" style="--grid-min: 20rem; gap: 2rem; margin: 1.5rem 0;">
  <div class="activity-image-container">
    <img src="/assets/images/gallery/Aso%20Drive%20Map.png" alt="Aso Drive Map" class="clickable-image" data-fullsrc="/assets/images/gallery/Aso%20Drive%20Map.png">
  </div>
</div>

### ⚔️ Kendo Practice
Experience the traditional Japanese martial art of Kendo. Learn the fundamentals of this disciplined practice that combines physical training with mental focus and respect. [Download Kendo Practice Information (PDF)](/assets/PDFs/Kendo%20Practice.pdf){target="_blank" rel="noopener noreferrer"}

<div class="grid" style="--grid-min: 20rem; gap: 2rem; margin: 1.5rem 0;">
  <div class="activity-image-container">
    <img src="/assets/images/gallery/Kendo%20Practice.png" alt="Kendo Practice" class="clickable-image" data-fullsrc="/assets/images/gallery/Kendo%20Practice.png">
  </div>
</div>

### ♨️ Kurokawa Onsen
Relax and rejuvenate at the famous Kurokawa Onsen, one of Japan's most beautiful hot spring towns. Experience the traditional Japanese bathing culture in a serene, natural setting. [Download Kurokawa Onsen Information (PDF)](/assets/PDFs/Kurokawa%20Onsen.pdf){target="_blank" rel="noopener noreferrer"}

<div class="grid" style="--grid-min: 20rem; gap: 2rem; margin: 1.5rem 0;">
  <div class="activity-image-container">
    <img src="/assets/images/gallery/Kurokawa%20Onsen.png" alt="Kurokawa Onsen" class="clickable-image" data-fullsrc="/assets/images/gallery/Kurokawa%20Onsen.png">
  </div>
</div>

### 🍜 Soba Noodle Workshop
Learn to make traditional Japanese soba noodles from scratch! This hands-on workshop will teach you the art of soba making, followed by enjoying your freshly made noodles. [Download Soba Noodle Workshop Information (PDF)](/assets/PDFs/Soba%20Noodle%20Workshop.pdf){target="_blank" rel="noopener noreferrer"}

<div class="grid" style="--grid-min: 20rem; gap: 2rem; margin: 1.5rem 0;">
  <div class="activity-image-container">
    <img src="/assets/images/gallery/Soba%20Noodle%20Workshop.png" alt="Soba Noodle Workshop" class="clickable-image" data-fullsrc="/assets/images/gallery/Soba%20Noodle%20Workshop.png">
  </div>
</div>

### 🏴‍☠️ One Piece Tour
Embark on an exciting adventure inspired by the popular anime and manga series One Piece! Explore themed locations and experience the world of pirates and adventure in this unique cultural tour. [Download One Piece Tour Information (PDF)](/assets/PDFs/One%20Piece%20Tour.pdf){target="_blank" rel="noopener noreferrer"}

<div class="grid" style="--grid-min: 20rem; gap: 2rem; margin: 1.5rem 0;">
  <div class="activity-image-container">
    <img src="/assets/images/gallery/One%20Piece%20Tour.png" alt="One Piece Tour" class="clickable-image" data-fullsrc="/assets/images/gallery/One%20Piece%20Tour.png">
  </div>
</div>

## Experience Authentic Japan

These activities are carefully selected to provide you with authentic cultural experiences that complement your school immersion. Each activity offers unique insights into Japanese traditions, nature, and way of life.

For more details about scheduling and participation, please refer to the program itinerary or contact us directly.

<!-- Image Modal -->
<div id="imageModal" style="display: none; position: fixed; z-index: 1000; left: 0; top: 0; width: 100%; height: 100%; background-color: rgba(0,0,0,0.9); cursor: pointer;">
  <div style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 95%; height: 95%; display: flex; align-items: center; justify-content: center;">
    <img id="modalImage" src="" alt="" style="max-width: 100%; max-height: 100%; width: auto; height: auto; border-radius: 8px; object-fit: contain;">
  </div>
  <div style="position: absolute; top: 20px; right: 35px; color: #fff; font-size: 40px; font-weight: bold; cursor: pointer;">&times;</div>
</div>

<script>
  document.addEventListener('DOMContentLoaded', function() {
    const images = document.querySelectorAll('.clickable-image');
    const modal = document.getElementById('imageModal');
    const modalImg = document.getElementById('modalImage');
    const closeBtn = modal.querySelector('div:last-child');

    images.forEach(function(img) {
      img.addEventListener('click', function() {
        modal.style.display = 'block';
        modalImg.src = this.getAttribute('data-fullsrc');
        modalImg.alt = this.alt;
      });
    });

    closeBtn.addEventListener('click', function() {
      modal.style.display = 'none';
    });

    modal.addEventListener('click', function(e) {
      if (e.target === modal) {
        modal.style.display = 'none';
      }
    });

    document.addEventListener('keydown', function(e) {
      if (e.key === 'Escape' && modal.style.display === 'block') {
        modal.style.display = 'none';
      }
    });
  });
</script>

