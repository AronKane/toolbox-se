<script setup>

import Test  from './Test.vue'
import { ref } from "vue";
import {
    NLoadingBarProvider, NMessageProvider, NNotificationProvider, NDialogProvider,
    NLayout, NLayoutHeader, NLayoutFooter, NLayoutSider, NLayoutContent, NH2,
    NButton, NDatePicker, NInput, NInputGroup
} from 'naive-ui'

import MainPage from './MainPage.vue'
</script>

<template>
    <n-loading-bar-provider>
        <n-message-provider>
            <n-notification-provider>
                <n-dialog-provider>
                    <n-layout position="absolute">
                        <n-layout-header style="height: 64px; padding: 24px" bordered>Yiheyuan Road</n-layout-header>
                        <n-layout has-sider position="absolute" style="top: 64px; bottom: 64px">
                            <n-layout-sider
                                bordered
                                content-style="padding: 24px;"
                                show-trigger="arrow-circle"
                            >Handian Bridge</n-layout-sider>
                            <n-layout content-style="padding: 24px;">
                                <MainPage />
                            </n-layout>
                        </n-layout>
                        <n-layout-footer
                            bordered
                            position="absolute"
                            style="height: 64px; padding: 24px"
                        >footer</n-layout-footer>
                    </n-layout>
                </n-dialog-provider>
            </n-notification-provider>
        </n-message-provider>
    </n-loading-bar-provider>
</template>

<style scoped>
a {
    color: #42b983;
}

.home {
    height: 100%;
}
</style>
