<template>
    <main class="container">
        <div class="card my-4 col-8 mx-auto">
            <div class="card-header">Login Form</div>
            <div class="card-body">
                <form @submit.prevent="login">
                    <div class="form-group">
                        <label for="" class="form-label">E-mail</label>
                        <input v-model="user.email" type="email" class="form-control" required autofocus>
                    </div>
                    <div class="form-group">
                        <label for="" class="form-label">Password</label>
                        <input v-model="user.password" type="password" class="form-control" required>
                    </div>
                    <button class="btn btn-primary my-2" type="submit">Login</button>
                </form>
            </div>
        </div>
    </main>
</template>

<script>
import authStore from '@/store/auth'
import { useRouter } from 'vue-router'
import { reactive } from 'vue'

export default {
    setup() {
        const router = useRouter();
        const user = reactive({
            email:'',
            password: ''
        })

        let login = async () => {
            await authStore.dispatch('login', user)
            router.replace({
                name: 'Dashboard'
            })
        }

        return { user , login}
    }
}
</script>

<style>

</style>