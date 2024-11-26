<script>
    import PostCard from './components/PostCard.vue'
    const data = def([])
    fetch('https://jsonplaceholder.typicode.com/posts')
    .then(resp=>resp.json())
    .then((d)=>data=d)
    .finally(()=>console.log('end api'))
    
</script>

<template>
    <h5 class="display-5">Home post</h5>
    <hr>
    <button class="btn btn-primary">Next</button>
    <button class="btn btn-primary">Previous</button>

    <PostCard v-for ="p in data":key="p.id"
        :id="p.id"
        :title="p.title"
        :body="p.body"
        >
    </PostCard>
</template>
