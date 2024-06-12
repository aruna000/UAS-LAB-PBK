<template>
  <div>
    <h1>Daftar Tugas</h1>
    <div class="border">
      <ul class="task-list">
        <li v-for="(task, index) in tasks" :key="index">
          <a
            :href="links[index]"
            class="task-button"
            @click.prevent="kelink(links[index])"
            >{{ task }}</a
          >
          <hr class="task-divider" />
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      tasks: [
        "Tugas 1",
        "Tugas 2",
        "Tugas 3",
        "Tugas 4",
        "Tugas 5",
        "Tugas 6",
        "Tugas 7",
      ],
      links: [
        "https://fajar-project-cv.vercel.app/",
        "https://fajarmuhairi-223510258-tugas2.vercel.app/",
        "https://fajar-muhairi-223510258-tugas3.vercel.app/",
        "https://fajar-muhairi-223510258-tugas4.vercel.app/",
        "https://valoshopbyfajar-fajars-projects-2e8f15d5.vercel.app/",
        "https://fajarmuhairi-223510258-tugas6.vercel.app/",
        "https://tugas7-fajar.vercel.app/",
      ],
    };
  },
  methods: {
    kelink(link) {
      window.open(link, "_blank");
    },
  },
};
</script>

<style scoped>
.container {
  position: relative;
  max-width: 480px;
  width: 100%;
  border-radius: 8px;
  padding: 25px;
  margin: 85px auto 0;
  background-color: rgba(255, 255, 255, 0.85);
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
  color: #383737;
}

h1 {
  text-align: center;
  margin-bottom: 20px;
  font-size: 28px;
  color: #383737;
}

.border {
  border: 1px solid #ccc;
  border-radius: 8px;
}

.task-list {
  list-style: none;
  padding: 0;
  margin: 0;
  font-weight: bold;
  opacity: 0.8;
}

.task-button {
  display: block;
  background-color: #ffffff;
  color: #383737;
  padding: 15px 20px;
  border-radius: 8px;
  text-decoration: none;
  margin-bottom: 1px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  transition: background-color 0.3s, transform 0.2s;
}

.task-button:hover {
  background-color: #f0f0f0;
  transform: translateY(-2px);
}

.task-divider {
  border: none;
  border-top: 0.5px solid #ccc;
  margin: 0;
}
</style>
