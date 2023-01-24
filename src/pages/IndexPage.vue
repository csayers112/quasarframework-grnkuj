<template>
  <q-page class="column flex-center">
    <div id="q-app" style="min-height: 100vh">
      <div class="row justify-center">
        <div class="col-md-5 col-lg-5 col-xs-12 col-sm-12">
          <div class="top-image" style="margin-top: -10px"></div>
        </div>

        <div class="col-md-7 col-lg-7 col-xs-12 col-sm-12">
          <div class="q-pa-md content">
            <div class="col-md-6 col-lg-6 col-xl-6 col-sm-12 col-xs-12">
              <div id="q-app" style="min-height: 100vh">
                <div class="">
                  <q-stepper
                    v-model="step"
                    ref="stepper"
                    contracted
                    color="primary"
                    animated
                  >
                    <q-step
                      :name="1"
                      title="Select campaign settings"
                      icon="settings"
                      :done="step > 1"
                    >
                      <p class="eyebrow-text">WELCOME TO BETTER</p>
                      <h1 class="main-headline">
                        Let’s get you up and running.
                      </h1>
                      <p style="font-size: 20px">
                        We promised you simple. Now we prove it.
                      </p>
                      <p>Start by talking with your contractor adviser.</p>

                      <q-btn
                        color="secondary"
                        icon="event"
                        class="full-width"
                        label="Talk to us"
                      ></q-btn>
                      <div style="text-align: center" class="justify-center">
                        <q-btn
                          flat
                          color="secondary"
                          label="Get your link"
                          icon-right="navigate_next"
                        />
                      </div>

                      <br />
                      <br />
                      <p class="eyebrow-text">GET YOUR TOOLS</p>

                      <q-list>
                        <q-item
                          @click="$refs.stepper.goTo(2)"
                          clickable
                          v-ripple
                        >
                          <q-item-section
                            >Grab your link to share with
                            customers</q-item-section
                          >
                          <q-item-section avatar>
                            <q-icon color="primary" name="navigate_next" />
                          </q-item-section>
                        </q-item>

                        <q-item
                          @click="$refs.stepper.goTo(3)"
                          clickable
                          v-ripple
                        >
                          <q-item-section
                            >Book a call with a contractor
                            adviser</q-item-section
                          >
                          <q-item-section avatar>
                            <q-icon color="primary" name="navigate_next" />
                          </q-item-section>
                        </q-item>

                        <q-item @click="$refs.stepper.goTo(3)" clickable v-ripple>
                          <q-item-section
                            >Learn how to talk about financing</q-item-section
                          >
                          <q-item-section avatar>
                            <q-icon color="primary" name="navigate_next" />
                          </q-item-section>
                        </q-item>

                        <q-item clickable v-ripple>
                          <q-item-section
                            >See what your customer sees</q-item-section
                          >
                          <q-item-section avatar>
                            <q-icon color="primary" name="navigate_next" />
                          </q-item-section>
                        </q-item>

                        <q-item clickable v-ripple>
                          <q-item-section
                            >Snag a cheatsheet to answer
                            questions</q-item-section
                          >
                          <q-item-section avatar>
                            <q-icon color="primary" name="navigate_next" />
                          </q-item-section>
                        </q-item>

                        <q-item clickable v-ripple>
                          <q-item-section>Open your portal</q-item-section>
                          <q-item-section avatar>
                            <q-icon color="primary" name="navigate_next" />
                          </q-item-section>
                        </q-item>
                      </q-list>
                    </q-step>

                    <q-step
                      :name="2"
                      title="Get your link"
                      caption="Optional"
                      icon="create_new_folder"
                      :done="step > 2"
                    >
                      <p class="eyebrow-text">BRING ON THE APPLICATIONS</p>
                      <h1 class="main-headline">Good choices start here.</h1>
                      <p style="font-size: 20px">
                        This is the link you’ll share with your customers so
                        they can check for pre-qualified loan offers, without
                        impacting their credit. You’ll also find it in your
                        portal.
                      </p>

                      <q-banner class="bg-grey-3">
                        <template v-slot:avatar>
                          <q-icon name="tips_and_updates" color="primary" />
                        </template>
                        <b>Pro tip </b><p>Bookmark this link on the homepage of your
                        phone to keep it handy.</p>
                      </q-banner>
<br />
                      <q-input
                        outlined
                        v-model="text"
                        placeholder="acornfinance.com/apply/EWY"
                        text="acornfinance.com/apply/EWY"
                      >
                        <template v-slot:append>
                          <q-icon name="file_copy" color="accent" />
                        </template>
                      </q-input>

                      <br />
                      <br />
                      <p class="eyebrow-text">HOW TO USE YOUR LINK</p>

                      <q-timeline
                        :layout="layout"
                        :side="side"
                        color="secondary"
                      >
                        <!-- <q-timeline-entry heading>How to use your link</q-timeline-entry>-->

                        <q-timeline-entry
                          title=""
                          subtitle="step 1"
                          side="left"
                          icon="content_copy"
                        >
                          <div class="timeline-text-lg">
                            Copy the link above, and paste it into a text or
                            email to your customer.
                          </div>
                        </q-timeline-entry>

                        <q-timeline-entry
                          title=""
                          subtitle="Step 2"
                          side="right"
                          icon="ads_click"
                        >
                          <div class="timeline-text-lg">
                            They’ll click the link to see their financing
                            options, using their phone or computer.
                          </div>
                        </q-timeline-entry>

                        <q-timeline-entry
                          title=""
                          subtitle="Step 3"
                          side="left"
                          icon="phone_iphone"
                        >
                          <div class="timeline-text-lg">
                            Keep your link handy so you can use it when you need
                            it.
                          </div>
                        </q-timeline-entry>
                      </q-timeline>
                    </q-step>

                    <q-step :name="3" 
                              title="Book a meeting" 
                              icon="add_comment">

                              <p class="eyebrow-text">BOOK A MEETING</p>
                              <h1 class="main-headline">Let’s talk it out.</h1>
                              <p style="font-size: 20px">
                                Schedule a call with an expert contractor adviser who knows what your day to day is like—so you can make your big picture bigger.
                              </p>

                          
                             <iframe src="https://calendly.com/corey-244/30min?month=2023-01" scrolling="no" title="" style="border:none;" width="100%" height="1000"></iframe>

                      
                    </q-step>




                    <q-step :name="4" 
                              title="Talk about Financing" 
                              icon="add_comment">

                              <p class="eyebrow-text">PREVIEW THE PROCESS</p>
                              <h1 class="main-headline">Know what’s coming.</h1>
                              <p style="font-size: 20px">
                                See what your customers see when they click on your application link.
                              </p>
                              <p class="eyebrow-text">HOW TO USE YOUR LINK</p>

                              <q-timeline
                                :layout="layout"
                                :side="side"
                                color="secondary"
                              >
                                <!-- <q-timeline-entry heading>How to use your link</q-timeline-entry>-->

                                <q-timeline-entry
                                  title="They get your link."
                                  subtitle="step one"
                                  side="left"
                                >
                                  <div class="">
                                    In an estimate, an invoice, an email, or in the room—you share, they click.
                                  </div>
                                </q-timeline-entry>

                                <q-timeline-entry
                                  title="They check for offers."
                                  subtitle="Step two"
                                  side="right"
                                  
                                >
                                  <div class="">
                                    TA short online form asks a few questions to see which offers they’re prequalified for from our 12+ lending partners, tailored to their credit profile. Each step explains what we need to know and why, with a support number for extra help. Looking for options is a soft credit pull, which means their credit won’t be affected.
                                  </div>
                                </q-timeline-entry>

                                <q-timeline-entry
                                  title="They apply with a lender."
                                  subtitle="Step three"
                                  side="left"
                                 
                                >
                                  <div class="">
                                    If they see an offer that works for them, they select it, and apply directly with the lender. Some lenders require a hard credit pull for this step, so we’re getting a little more committed.
                                  </div>
                                </q-timeline-entry>

                                <q-timeline-entry
                                  title="They get funded."
                                  subtitle="Step four"
                                  side="left"
                                  
                                >
                                  <div class="">
                                    If they’re approved, they’ll get their money as soon as the same day.* (It can take a little longer for larger amounts.) They pay you, you do the work, and it all starts again.
                                  </div>
                                </q-timeline-entry>



                              </q-timeline>
                        
                      
                    </q-step>







                    <template v-slot:navigation>
                      <q-stepper-navigation>
                        <q-btn
                          @click="$refs.stepper.next()"
                          color="primary"
                          :label="step === 3 ? 'Finish' : 'Continue'"
                        ></q-btn>
                        <q-btn
                          v-if="step > 1"
                          flat
                          color="primary"
                          @click="$refs.stepper.previous()"
                          label="Back"
                          class="q-ml-sm"
                        ></q-btn>
                      </q-stepper-navigation>
                    </template>
                  </q-stepper>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </q-page>
</template>

<script>
import { ref } from 'vue';

export default {
  setup() {
    return {
      step: ref(1),
    };
  },
};

import { copyToClipboard } from 'quasar';

copyToClipboard('some text')
  .then(() => {
    // success!
  })
  .catch(() => {
    // fail
  });
  
</script>


