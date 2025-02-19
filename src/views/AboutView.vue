<template>
  <main class="about-us">
    <div class="container">
      <div class="about-container">
        <h1>O nas</h1>
        <p class="description">
          Jesteśmy pasjonatami nowych technologii i innowacji, tworzymy rozwiązania, które zmieniają sposób, w jaki ludzie korzystają z usług.
        </p>

        <h2 id="bottom" class="team-title">Nasza misja</h2>
        <p>
          Naszym celem jest stworzenie porównywarki cen paliw. Aplikacji umożliwiającej użytkownikom przeglądanie listy oraz mapy stacji paliwowych z
          filtrami według m.in. marki, rodzaju paliwa i ceny. Użytkownicy mogą zgłaszać ceny paliw a administratorzy zarządzają użytkownikami, stacjami
          oraz zgłoszonymi cenami. Aplikacja umożliwia nagradzanie użytkowników dodatkowymi punktami.
        </p><br><br>

      </div>
    </div>
  </main>
</template>
<script>
export default {
  mounted() {
    // Sprawdzamy, czy na URL jest hash, który wskazuje na element
    if (window.location.hash === "#bottom") {
      // Jeśli tak, przewijamy do tego elementu
      const element = document.getElementById("bottom");
      if (element) {
        element.scrollIntoView({ behavior: "smooth" });
      }
    }
  }
};
</script>
<style scoped>
.about-us {
  padding: 20px;
  background-image: url('@/assets/tło2.jpg');
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
  color: white;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

.about-container {
  background-color: rgba(0, 0, 0, 0.5); /* Ciemne półprzezroczyste tło */
  padding: 40px;
  border-radius: 8px;
  margin-bottom: 40px;
  width: 100%;
  max-width: 800px;
  margin-left: auto;
  margin-right: auto;
}

h1 {
  text-align: center;
  color: #fff;
}

.description {
  font-size: 18px;
  text-align: center;
  margin: 20px 0;
  color: #fff;
}

.description_small {
  font-size: 8px;
  text-align: center;
  margin: 20px 0;
  color: #fff;
}

.divider {
  border: 0;
  border-top: 2px solid black;
  margin: 40px 0;
}

.team-section {
  margin-top: 40px;
}

.team-title {
  text-align: center;
  margin-bottom: 60px;
}

.team-members {
  display: flex;
  justify-content: space-between;
  gap: 20px;
  flex-wrap: wrap;
}

.team-member {
  text-align: center;
  flex: 1 1 calc(50% - 20px);
  max-width: calc(50% - 20px);
  margin-bottom: 40px;
}

.team-member h3 {
  color: #fff;
}

.team-photo {
  width: 150px;
  height: 150px;
  border-radius: 50%;
  object-fit: cover;
}

.mission-section {
  margin-top: 40px;
  background-color: #fff;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  text-align: center;
}

.mission-section h2 {
  color: #333;
}

.mission-section p {
  color: #555;
}
</style>
