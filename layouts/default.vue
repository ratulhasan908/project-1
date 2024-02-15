<template>
    <div class="flex h-screen font-roboto dashboard-body">
        <Sidebar />
        <div class="flex-1 flex flex-col overflow-hidden">
            <main class="flex-1 overflow-x-hidden overflow-y-auto bg-gray-200">
                <div class="main-body-layout mx-0 px-6 py-8">
                    <slot />
                </div>
            </main>
        </div>
    </div>
</template>