<script lang="ts">
export default {
  props: [],
  methods: {},
};
</script>
<script setup lang="ts">
import Swal from "sweetalert2";
const desc = `  <div class="">
    <p class="font-mono text-primary xl:text-xl text-lg font-semibold">
      Introduction
    </p>
    <ul
      class="ml-2 font-base lg:text-base text-sm text-primary-focus break-words list-disc list-inside"
    >
      <li>Gallery ที่สุ่ม Photo มาจำนวน 9 รูป</li>
      <li>แต่ละรูปมีปุ่มกดชอบ และ ไม่ชอบ รวมถึงชื่อคนถ่าย/ถือลิขสิทธ์</li>
      <li>
        แต่ละรูปจะสามารถกดชอบ หรือ ไม่ชอบได้ซึ่งสามารถนับจำนวนรวมทั้งหมดได้
      </li>
      <li>สามารถ random ภาพได้ทุกเมื่อ</li>
      <p class="font-mono text-accent xl:text-xl text-lg font-semibold">
        API Usage
      </p>
    </ul>
    <ul
      class="ml-2 font-base lg:text-base text-sm text-accent-focus break-words list-disc list-inside"
    >
      <li>ดึง API จาก Pexels Website (Pexels API) ในการแสดงผลรูปภาพ</li>
      <li>
        รูปภาพที่ถูกโหลดมาอาจต้องใช้เวลาซักเล็กหน่อยในการแสดงผลให้ครบทุกภาพ (9
        ภาพ)
      </li>
    </ul>
  </div>`;

const onShowInfo = () => {
  Swal.fire({
    title: "About Application",
    html: desc,
    icon: "info",
    confirmButtonText: "OK",
    footer: "Creator: นายพีรพัฒน์ บางขัน 6404101329",
  });
};
</script>
<template>
  <div class="fixed top-0 z-10 navbar bg-base-300">
    <div class="flex-1">
      <a class="logo-font btn btn-ghost normal-case text-2xl"
        ><u>Oat</u>Gallery</a
      >
    </div>
    <div class="flex-none">
      <button @click="onShowInfo" class="btn btn-square btn-ghost">
        <i class="fa-solid text-info fa-circle-question fa-2xl"></i>
      </button>
    </div>
  </div>
</template>
<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Lobster&family=Nanum+Gothic&family=Roboto:wght@500&display=swap");
.logo-font {
  font-family: "Lobster", cursive;
}
</style>
