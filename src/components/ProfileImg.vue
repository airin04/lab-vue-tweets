<template>
  <img :src="image" className="profile"
  alt="profile image"/>
</template>

<script>
export default {
   props: {
    image: String,
    },
};
</script>
