<template>
    <div class="projects">
        <h2>Projects</h2>
        <div v-for="project in projects" :key="project.id" class="project-card">
            <h3>{{ project.title }}</h3>
            <p>{{ project.description }}</p>
            <a :href="project.link" target="_blank">View Project</a>
        </div>
    </div>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          id: 1,
          title: 'Task 1',
          description: 'Task 1 of SIT120',
          link: 'https://example.com/project1',
        },
        {
          id: 2,
          title: 'Task 2',
          description: 'Task 2 of SIT120',
          link: 'https://example.com/project2',
        },
        // Add more project objects as needed
      ],
    };
  },
};
</script>

<style scoped>
    /* Add CSS styles for the projects component here */
    .projects {
        /* Add styles for the projects container */
    }

    .project-card {
        /* Add styles for each project card */
    }
</style>
