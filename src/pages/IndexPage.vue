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
                <div class="" ref="top">
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
                      <q-banner class="bg-grey-3">
                        <template v-slot:avatar>
                          <q-icon name="tips_and_updates" color="primary" />
                        </template>
                        <b>Pro tip </b>
                        <p>
                          Book a call with a contractor adviser is the easiest
                          way to get started.
                        </p>
                      </q-banner>
                      <br />
                      <q-btn
                        color="secondary"
                        icon="event"
                        class="full-width"
                        label="Talk to us"
                        @click="
                            $refs.stepper.goTo(3);
                            $router.replace('#top');
                          "
                      ></q-btn>
                      <div style="text-align: center" class="justify-center">
                        <q-btn
                          flat
                          color="secondary"
                          label="Get your link"
                          icon-right="navigate_next"
                           @click="
                            $refs.stepper.goTo(2);
                            $router.replace('#top');
                          "
                        />
                      </div>

                      <br />
                      <br />
                      <p class="eyebrow-text">GET YOUR TOOLS</p>

                      <q-list>
                        <q-item
                          @click="
                            $refs.stepper.goTo(2);
                            $router.replace('#top');
                          "
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
                          @click="
                            $refs.stepper.goTo(3);
                            $router.replace('#top');
                          "
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

                        <q-item
                          @click="
                            $refs.stepper.goTo(4);
                            $router.replace('#top');
                          "
                          clickable
                          v-ripple
                        >
                          <q-item-section
                            >Learn how to talk about financing</q-item-section
                          >
                          <q-item-section avatar>
                            <q-icon color="primary" name="navigate_next" />
                          </q-item-section>
                        </q-item>

                        <q-item
                          @click="
                            $refs.stepper.goTo(5);
                            $router.replace('#top');
                          "
                          clickable
                          v-ripple
                        >
                          <q-item-section
                            >See what your customer sees</q-item-section
                          >
                          <q-item-section avatar>
                            <q-icon color="primary" name="navigate_next" />
                          </q-item-section>
                        </q-item>

                        <q-item
                          @click="
                            $refs.stepper.goTo(6);
                            $router.replace('#top');
                          "
                          clickable
                          v-ripple
                        >
                          <q-item-section
                            >Snag a cheatsheet to answer
                            questions</q-item-section
                          >
                          <q-item-section avatar>
                            <q-icon color="primary" name="navigate_next" />
                          </q-item-section>
                        </q-item>

                        <q-item
                          @click="
                            $refs.stepper.goTo(6);
                            $router.replace('#top');
                          "
                          clickable
                          v-ripple
                        >
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
                        <b>Pro tip </b>
                        <p>
                          Bookmark this link on the homepage of your phone to
                          keep it handy.
                        </p>
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
                          title="Get your link."
                          subtitle="step one"
                          side="left"
                          icon="content_copy"
                        >
                          <div class="timeline-text-lg">
                            Copy the link above, and paste it into a text or
                            email to your customer.
                          </div>
                        </q-timeline-entry>

                        <q-timeline-entry
                          title="Send it to your customer."
                          subtitle="Step two"
                          side="right"
                          icon="ads_click"
                        >
                          <div class="timeline-text-lg">
                            They’ll click the link to see their financing
                            options, using their phone or computer.
                          </div>
                        </q-timeline-entry>

                        <q-timeline-entry
                          title="Save it for later."
                          subtitle="Step three"
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

                    <q-step
                      :name="3"
                      title="Book a meeting"
                      icon="add_comment"
                      :done="step > 3"
                    >
                      <p class="eyebrow-text">BOOK A MEETING</p>
                      <h1 class="main-headline">Let’s talk it out.</h1>
                      <p style="font-size: 20px">
                        Schedule a call with an expert contractor adviser who
                        knows what your day to day is like—so you can make your
                        big picture bigger.
                      </p>

                      <iframe
                        src="https://calendly.com/corey-244/30min?month=2023-01"
                        scrolling="no"
                        title=""
                        style="border: none"
                        width="100%"
                        height="1000"
                      ></iframe>
                    </q-step>

                    <q-step
                      :name="4"
                      title="Talk about Financing"
                      icon="add_comment"
                      :done="step > 4"
                    >
                      <p class="eyebrow-text">PREVIEW THE PROCESS</p>
                      <h1 class="main-headline">Know what’s coming.</h1>
                      <p style="font-size: 20px">
                        See what your customers see when they click on your
                        application link.
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
                            In an estimate, an invoice, an email, or in the
                            room—you share, they click.
                            <br />
                            <img
                              src="/src/assets/graphic-1.png"
                              style="
                                width: 100%;
                                max-width: 400px !important;
                                height: auto;
                                margin-bottom: 40px;
                                margin-top: 20px;
                                margin-left: auto;
                                margin-right: auto;
                              "
                            />
                          </div>
                        </q-timeline-entry>

                        <q-timeline-entry
                          title="They check for offers."
                          subtitle="Step two"
                          side="right"
                        >
                          <div class="">
                            TA short online form asks a few questions to see
                            which offers they’re prequalified for from our 12+
                            lending partners, tailored to their credit profile.
                            Each step explains what we need to know and why,
                            with a support number for extra help. Looking for
                            options is a soft credit pull, which means their
                            credit won’t be affected.
                            <br />
                            <img
                              src="/src/assets/graphic-2.png"
                              style="
                                width: 100%;
                                max-width: 200px !important;
                                height: auto;
                                margin-bottom: 40px;
                                margin-top: 20px;
                                margin-left: auto;
                                margin-right: auto;
                              "
                            />
                          </div>
                        </q-timeline-entry>

                        <q-timeline-entry
                          title="They apply with a lender."
                          subtitle="Step three"
                          side="left"
                        >
                          <div class="">
                            If they see an offer that works for them, they
                            select it, and apply directly with the lender. Some
                            lenders require a hard credit pull for this step, so
                            we’re getting a little more committed.
                            <br />
                            <img
                              src="/src/assets/graphic-3.png"
                              style="
                                width: 100%;
                                max-width: 200px !important;
                                height: auto;
                                margin-bottom: 40px;
                                margin-top: 20px;
                                margin-left: auto;
                                margin-right: auto;
                              "
                            />
                          </div>
                        </q-timeline-entry>

                        <q-timeline-entry
                          title="They get funded."
                          subtitle="Step four"
                          side="left"
                        >
                          <div class="">
                            If they’re approved, they’ll get their money as soon
                            as the same day.* (It can take a little longer for
                            larger amounts.) They pay you, you do the work, and
                            it all starts again.
                            <br />
                            <img
                              src="/src/assets/graphic-4.png"
                              style="
                                width: 100%;
                                max-width: 200px !important;
                                height: auto;
                                margin-bottom: 40px;
                                margin-top: 20px;
                                margin-left: auto;
                                margin-right: auto;
                              "
                            />
                          </div>
                        </q-timeline-entry>
                      </q-timeline>
                    </q-step>

                    <q-step
                      :name="5"
                      title="Talk about Financing"
                      icon="add_comment"
                      :done="step > 5"
                    >
                      <p class="eyebrow-text">SAVE SOME SHORTCUTS</p>
                      <h1 class="main-headline">When they ask, answer.</h1>
                      <p style="font-size: 20px">
                        Keep this quick info handy, in case your customers want
                        to understand more about financing.
                      </p>
                      <br />
                      <br />
                      <p class="eyebrow-text">FREQUENTLY ASKED QUESTIONS</p>

                      <q-list>
                        <q-expansion-item
                          expand-separator
                          label="Who is Acorn Finance"
                        >
                          <q-card>
                            <q-card-section>
                              <p>
                                Acorn Finance is a lending marketplace where the
                                nation’s premier online consumer lenders
                                pre-qualify customers for personalized loan
                                options in 60 seconds, with no impact to the
                                homeowner’s credit score. Acorn Finance uses an
                                initial soft credit inquiry to provide access to
                                competitive, fixed-rate loans through a fast and
                                easy online process.
                              </p>
                            </q-card-section>
                          </q-card>
                        </q-expansion-item>

                        <q-expansion-item
                          expand-separator
                          label="What types of lending options are available?"
                        >
                          <q-card>
                            <q-card-section>
                              <p>
                                Depending on the lender that fits you best, you
                                may be offered a personal loan or personal line
                                of credit.
                              </p>

                              <p>
                                A personal loan lets you borrow money now and
                                pay it back over time with fixed monthly
                                payments. Personal loans have fixed rates of
                                interest and typically have terms ranging from 2
                                to 12 years. They may be unsecured (no
                                collateral) or secured (collateral required).
                              </p>

                              <p>
                                A personal line of credit allows you to borrow
                                at any time based on a preset limit. As long as
                                your account is open and your credit remains in
                                good standing, you can borrow up to the maximum
                                amount and pay interest only on the amount you
                                actually borrow.
                              </p>
                            </q-card-section>
                          </q-card>
                        </q-expansion-item>

                        <q-expansion-item
                          expand-separator
                          label="How much can be borrowed?"
                        >
                          <q-card>
                            <q-card-section>
                              <p>
                                Acorn Finance's network of lenders offers loans
                                from $2,000 to $100,000 for qualified borrowers.
                              </p>
                            </q-card-section>
                          </q-card>
                        </q-expansion-item>

                        <q-expansion-item
                          expand-separator
                          label="What can the funds be used for?"
                        >
                          <q-card>
                            <q-card-section>
                              <p>
                                Anything. For instance, your purchase with us.
                              </p>
                            </q-card-section>
                          </q-card>
                        </q-expansion-item>

                        <q-expansion-item
                          expand-separator
                          label="How long does it take to get approved?"
                        >
                          <q-card>
                            <q-card-section>
                              <p>
                                Qualified applicants can be approved quickly
                                during business hours and may receive their
                                funds as soon as within 1 business day.
                              </p>
                            </q-card-section>
                          </q-card>
                        </q-expansion-item>

                        <q-expansion-item
                          expand-separator
                          label="Are there any fees?"
                        >
                          <q-card>
                            <q-card-section>
                              <p>
                                Acorn Finance's lenders charge no penalties for
                                early repayment, and no processing fees on loans
                                of more than $40,000. If you borrow less than
                                $40,000, some lenders may charge an origination
                                fee between 1-6%. You’ll see no-fee options
                                clearly highlighted on your offers pages, so you
                                can make a fully informed choice.
                              </p>
                            </q-card-section>
                          </q-card>
                        </q-expansion-item>

                        <q-expansion-item
                          expand-separator
                          label="Can a co-borrower be included?"
                        >
                          <q-card>
                            <q-card-section>
                              <p>
                                Yes. Co-borrowers are encouraged to apply, and
                                can be added immediately after the initial
                                applicant submits their information.
                              </p>
                            </q-card-section>
                          </q-card>
                        </q-expansion-item>

                        <q-expansion-item
                          expand-separator
                          label="Does Acorn Finance cover all 50 states?"
                        >
                          <q-card>
                            <q-card-section>
                              <p>
                                Acorn Finance is available online throughout the
                                United States, except in MD, NJ, NV, WV, VT, and
                                RI – so far! You can check the current coverage
                                area at
                                https://www.acornfinance.com/acorn-finance-coverage/
                                to make sure your state is included.
                              </p>
                            </q-card-section>
                          </q-card>
                        </q-expansion-item>
                      </q-list>
                    </q-step>

                    <q-step
                      :name="6"
                      title="Head to the Portal"
                      icon="add_comment"
                      :done="step > 6"
                    >
                      <p class="eyebrow-text">CREATE YOUR ACCOUNT</p>
                      <h1 class="main-headline">Welcome to your portal.</h1>
                      <p style="font-size: 20px">
                        Here’s where you’ll find grab-and-go marketing assets,
                        training videos and materials, and a permanent home for
                        your application link. When you sign in, you’ll unlock
                        notifications of your customers’ progress as they apply
                        and get funded. Just choose a username and password.
                      </p>

                      <img
                        src="/src/assets/portal-image.png"
                        style="
                          width: 100%;
                          max-width: 600px !important;
                          height: auto;
                          margin-bottom: 40px;
                          margin-top: 20px;
                          margin-left: auto;
                          margin-right: auto;
                        "
                      />
                    </q-step>
                    
                    <template v-slot:navigation>
                      <q-stepper-navigation style="text-align:right;">
                        <q-btn
                          v-if="step > 1"
                          flat
                          color="primary"
                          @click="
                            $refs.stepper.previous();
                            $router.replace('#top');
                          "
                          label="Back"
                          class="q-ml-sm"
                        ></q-btn>

                        <q-btn
                          @click="
                            $refs.stepper.next();
                            $router.replace('#top');
                          "
                          color="primary"
                          :label="step === 6 ? 'My Portal' : 'Continue'"
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
import { copyToClipboard } from 'quasar';
import { scroll } from 'quasar';
import { Notify } from 'quasar';

export default {
  setup() {
    return {
      step: ref(1),
    };
  },
};

copyToClipboard('some text')
  .then(() => {
    // success!
  })
  .catch(() => {
    // fail
  });
</script>
