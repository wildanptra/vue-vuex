<template>
    <main class="container">
        <div class="card my-4 col-8 mx-auto">
            <div class="card-header">Login Form</div>
            <div class="card-body">
                <form>
                    <div class="form-group">
                        <label for="" class="form-label">E-mail</label>
                        <input type="email" class="form-control" required autofocus>
                    </div>
                    <div class="form-group">
                        <label for="" class="form-label">Password</label>
                        <input type="password" class="form-control" required>
                    </div>
                    <button class="btn btn-primary my-2" type="submit">Login</button>
                </form>
            </div>
        </div>
    </main>
</template>

<script>
export default {
    name: 'Login',
}
</script>

<style>

</style>