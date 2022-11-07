<template>
  <nav>
    <div>
      <h1><strong>ETDS CHAT APP</strong> </h1>

      <div v-if="isLogin" class="login">
        <Clique :src="user.photoURL" />
        <button class="text-gray-400 hover:text-red" @click="signOut">
          Sign Out
        </button>
      </div>

      <button v-else class="bg-blue-500 hover:bg-blue-600" @click="signIn">
        Sign in
      </button>
    </div>
  </nav>
</template>

<script>
import Clique from './Clique.vue'
import { useAuth } from '@/firebase'

export default {
  components: { Clique },
  setup() {
    const { user, isLogin, signOut, signIn } = useAuth()
    return { user, isLogin, signOut, signIn }
  }
}
</script>
