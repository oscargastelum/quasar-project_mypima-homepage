<template>
  <q-page>
    <div class="q-py-lg q-px-md row items-end q-col-gutter-md">
      <div class="col">
        <q-input
          bottom-slots
          v-model="newMyPimaContent"
          class="new-content"
          placeholder="Email a faculty member:"
          counter
          maxlength="280"
          autogrow
        >
          <template v-slot:before>
            <q-avatar size="xl">
              <img src="https://cdn.quasar.dev/img/avatar5.jpg" />
            </q-avatar>
          </template>
        </q-input>
      </div>
      <div class="col col-shrink">
        <q-btn
          :disable="!newMyPimaContent"
          round
          dense
          flat
          icon="send"
          class="q-mb-lg"
        />
      </div>
    </div>
    <q-separator size="10px" color="grey-2" class="divider"></q-separator>

    <q-list>
      <q-item class="q-py-md">
        <q-item-section avatar top>
          <q-avatar>
            <img src="https://cdn.quasar.dev/img/avatar2.jpg" />
          </q-avatar>
        </q-item-section>

        <q-item-section>
          <q-item-label class="text-subtitle1">
            <strong> ARC Resource Center </strong>
            <span class="text-grey-7">pcc-arcpantry@pima.edu</span>
          </q-item-label>
          <q-item-label class="MyPima-notification text-body1">
            Check out ARC Food Pantry at Pima Community College! If you're a
            currently enrolled student, you can visit us at West, Desert Vista,
            and East Campus during our hours of operation. Don't forget to bring
            your student ID or A#, as well as your student email upon arrival.
            You can receive one food bag per week that contain canned
            fruit/vegetables, boxed meals, breakfast items, beverages, and
            hygiene products upon request. For more information, email
            pcc-arcpantry@pima.edu or call 520.206.6720. #ARCfoodpantry
            #PimaCommunityCollege #foodsecurity
          </q-item-label>
        </q-item-section>

        <q-item-section side top> 1 min ago </q-item-section>
      </q-item>

      <q-item class="q-py-md">
        <q-item-section avatar top>
          <q-avatar>
            <img src="https://cdn.quasar.dev/img/avatar2.jpg" />
          </q-avatar>
        </q-item-section>

        <q-item-section>
          <q-item-label class="text-subtitle1">
            <strong> Health, Wellness and Safety </strong>
            <span class="text-grey-7"> infocenter@pima.edu</span>
          </q-item-label>
          <q-item-label class="MyPima-notification text-body1">
            Your well-being is our priority at Pima Community College. We're
            here to support you in any way we can, whether it's a medical
            emergency, personal crisis, or mental health concern. Call 911 for
            medical or safety emergencies, and the community crisis line at
            520.622.6000 for personal crises. For other concerns and agency
            referrals, call the Community Information & Referral Services within
            Arizona at 211. Our Dental Hygiene Clinic provides low-cost
            therapeutic and preventive services for dental care, and the
            on-campus Eastside Health Clinic is open to Pima students, staff,
            faculty, and the public. Find out more about the resources we offer
            for your health, wellness, and safety at Pima on our website.
          </q-item-label>
        </q-item-section>

        <q-item-section side top> 13 min ago </q-item-section>
      </q-item>

      <q-item class="q-py-md">
        <q-item-section avatar top>
          <q-avatar>
            <img src="https://cdn.quasar.dev/img/avatar2.jpg" />
          </q-avatar>
        </q-item-section>

        <q-item-section>
          <q-item-label class="text-subtitle1">
            <strong> Access & Disability Resources (ADR) </strong>
            <span class="text-grey-7">ADRhelp@pima.edu</span>
          </q-item-label>
          <q-item-label class="MyPima-notification text-body1">
            Need disability accommodations at Pima Community College? Access &
            Disability Resources (ADR) is here to help! We're now offering
            virtual office hours for your convenience. Contact us to learn more.
            #PimaADR #DisabilityAccommodations #VirtualOfficeHours
          </q-item-label>
        </q-item-section>

        <q-item-section side top> 54 min ago </q-item-section>
      </q-item>
    </q-list>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "PageHome",

  data() {
    return {
      newMyPimaContent: "",
    };
  },
});
</script>

<style lang="sass">
.new-content
  textarea
    font-size: 19px
    line-height: 1.4 !important

    .divider
    border-top: 1px solid
    border-bottom: 1px solid
    border-color: $grey-4

.MyPima-notification
  white-space: pre-line
</style>
