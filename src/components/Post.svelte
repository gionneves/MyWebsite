<script>
    export let id = 0;
    const db = require('better-sqlite3')('posts.db');
    const row = db.prepare('SELECT * FROM post WHERE id = ?').get(id);
</script>