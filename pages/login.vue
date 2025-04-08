<script setup>
import { LoaderCircle, UserCheck, CircleX } from "lucide-vue-next";

definePageMeta({
    layout: "login",
});
</script>

<template>
    <div class="min-h-screen flex items-center justify-center">
        <div class="mx-4 sm:mx-0 w-full sm:w-md">
            <Alert class="mb-4 variant-success-tonal">
                <UserCheck />
                <AlertTitle>Welcome back!</AlertTitle>
                <AlertDescription class="text-success"> Please wait... we're preparing the page for you! </AlertDescription>
            </Alert>
            <Alert class="mb-4 variant-error-tonal">
                <CircleX />
                <AlertTitle>Error!</AlertTitle>
                <AlertDescription class="text-error"> Something isn't correct with your username or password. </AlertDescription>
            </Alert>

            <Card>
                <CardHeader class="text-center">
                    <CardTitle class="text-xl">Student Portal</CardTitle>
                    <CardDescription>@High School of Indonesia</CardDescription>
                </CardHeader>
                <CardContent class="">
                    <!-- <form> -->
                    <Label class="mb-2">Username</Label>
                    <Input v-model="username" class="focus-visible:ring-2 focus-visible:ring-gray-900" required></Input>

                    <div class="mb-3"></div>

                    <Label class="mb-2">Password</Label>
                    <div class="mb-4 relative">
                        <Input v-model="password" class="focus-visible:ring-2 focus-visible:ring-gray-900 pr-[60px]" :type="showPassword ? 'text' : 'password'" required></Input>
                        <Button variant="link" size="icon" type="button" class="text-gray-500 absolute font-normal inset-y-0 right-0 mr-3" @click="this.showPassword = !this.showPassword">
                            {{ !showPassword ? "Show" : "Hide" }}
                        </Button>
                    </div>

                    <Button class="w-full cursor-pointer" @click="login()" :disabled="disableButton">
                        <template v-if="disableButton"> <LoaderCircle class="w-4 animate-spin" /> Please wait... </template>
                        <template v-else> Login </template>
                    </Button>
                    <!-- </form> -->
                </CardContent>
            </Card>
        </div>
    </div>
</template>

<script>
export default {
    data: () => ({
        username: "",
        password: "",

        showPassword: false,
        disableButton: false,
        isLoginSuccess: false,
    }),
    methods: {
        async login() {
            this.disableButton = true;
            const loginData = {
                username: this.username,
                password: this.password,
            };

            await new Promise((resolve) => setTimeout(resolve, 2000));

            this.isLoginSuccess = true;
            this.disableButton = false;
        },
    },
};
</script>
