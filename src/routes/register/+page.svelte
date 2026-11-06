<script lang="ts">
    import Logo from "#lib/assets/614d1097-0a5e-4738-8119-975b124dd369.webp";
    import Button from "#lib/components/button.svelte";
</script>

<svelte:head>
    <title>Login</title>
</svelte:head>
<main class="flex justify-center h-screen">
    <div class="space-y-6 min-w-md my-auto">
        <div class="mb-8">
            <enhanced:img
                src={Logo}
                class="rounded-sm size-12 mb-2"
                alt="Logo"
            />
            <h1 class="font-bold text-3xl">Welcome back!</h1>
            <h2 class="text-sm text-gray-500">We're happy to see you again</h2>
        </div>

        <div class="space-y-6">
            <fieldset class="flex flex-col gap-1">
                <label class="font-medium text-base" for="email">Email</label>
                <input
                    name="email"
                    class="rounded-sm border-gray-300 border px-2 py-1.5"
                    placeholder="Enter your email"
                    type="email"
                />
            </fieldset>
            <fieldset class="flex flex-col gap-1">
                <label class="font-medium text-base" for="password"
                    >Password</label
                >
                <input
                    name="password"
                    class="rounded-sm border-gray-300 border px-2 py-1.5"
                    placeholder="Enter your password"
                    type="password"
                />
            </fieldset>

            <fieldset class="flex flex-row gap-1 items-center">
                <input
                    name="advertising"
                    class="rounded-sm border-gray-300 appearance-none border size-4"
                    placeholder="Enter your password"
                    type="checkbox"
                />
                <p class="text-gray-500 text-sm">
                    I want to receive announcements and updates on my email
                </p>
            </fieldset>

            <div class="space-y-2 mt-8">
                <p class="text-gray-500 text-sm">
                    To register click <a
                        class="font-semibold text-black underline"
                        href="/">here</a
                    >, to recover your account
                    <a class="font-semibold text-black underline" href="/"
                        >here</a
                    >
                </p>

                <Button class="w-full">Submit</Button>
            </div>
        </div>
    </div>
</main>
