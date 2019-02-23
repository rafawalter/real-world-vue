<template>
  <div>
    <h1>Events listing</h1>
    <p>
      <router-link :to="{ name: 'event-show', params: { id: '1' } }"
        >First Event</router-link
      >
    </p>
  </div>
</template>
