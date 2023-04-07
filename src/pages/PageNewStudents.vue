<template>
  <q-page class="q-pa-lg">
    <h5 class="q-mt-none q-mb-md text-weight-bold">Getting Started at Pima</h5>

    <div class="person-container">
      <div class="person">
        <h5>Erica Martin</h5>
        <p>Academic Success Counselor</p>
        <p>Email: <a href="mailto:eamartin@pima.edu">eamartin@pima.edu</a></p>
        <p>Phone: (520)206-7242</p>
      </div>
      <div class="person">
        <h5>Guillermo Sandoval</h5>
        <p>Program Advisor</p>
        <p>
          Email: <a href="mailto:gsandoval9@pima.edu">gsandoval9@pima.edu</a>
        </p>
        <p>Phone: (520)206-6920</p>
      </div>
    </div>
    <div class="text-body1">
      <P class="q-mt-lg">
        Welcome new students to Pima Community College! We understand that
        starting college can be overwhelming, which is why we have dedicated
        academic success counselors and program advisors to help you navigate
        your academic journey. Erica Martin is our academic success counselor
        who can provide guidance on academic planning, career exploration, and
        personal support. Guillermo Sandoval is our program advisor who can
        provide information on degree programs, transfer options, and career
        opportunities. You can connect with Erica and Guillermo through
        PimaConnect, an online platform that allows you to schedule
        appointments, ask questions, and receive support. We are here to help
        you succeed, and we look forward to working with you throughout your
        time at Pima.</P
      >
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "PageNewStudents",
});
</script>

<style>
.person-container {
  display: flex;
  justify-content: space-between;
  margin-top: 10px;
}

.person {
  width: 45%;
  border: 1px solid #ccc;
  padding: 10px;
  border-radius: 5px;
}

.person h3 {
  margin-top: 0;
  font-size: 1.5rem;
}

.person p {
  margin-bottom: 5px;
  font-size: 1.2rem;
}
</style>
