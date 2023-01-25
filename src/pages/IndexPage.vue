<template>
  <q-page class="column flex-center">
    <div id="q-app" style="min-height: 100vh">
      <div class="row justify-center">
        <div
          class="showDesktop col-md-5 col-lg-5 col-xs-12 col-sm-12 order-last"
        >
          <div class="top-image" style="margin-top: -10px"></div>
        </div>
        <div
          class="showMobile col-md-5 col-lg-5 col-xs-12 col-sm-12 order-last"
        >
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
                    color="secondary"
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
                          Booking a call with a contractor adviser is the
                          easiest way to get started.
                        </p>
                        <div class="q-gutter-sm">
                          <q-btn
                          outline
                          color="accent"
                          label="Book a call"
                          icon-right="navigate_next"
                          @click="
                            $refs.stepper.goTo(3);
                            $router.replace('#top');
                          "
                        />
                        <q-btn
                          outline
                          color="accent"
                          label="Get your financing link"
                          icon-right="navigate_next"
                          @click="
                            $refs.stepper.goTo(2);
                            $router.replace('#top');
                          "
                        />
                        <br />
                        <br />
                        </div>
                      </q-banner>
                      <br />
                      <!--<q-btn
                        color="accent"
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
                          color="accent"
                          label="Get your link"
                          icon-right="navigate_next"
                          @click="
                            $refs.stepper.goTo(2);
                            $router.replace('#top');
                          "
                        />
                      </div>-->

                      <br />
                      <br />
                      <p class="eyebrow-text">WHAT WE'LL COVER</p>

                      <div class="showDesktop home-cards">
                        <div class="row q-col-gutter-x-md q-col-gutter-y-lg">
                          <div class="col-4">
                            <div class="q-card my-card">
                              <div
                                @click="
                                  $refs.stepper.goTo(2);
                                  $router.replace('#top');
                                "
                                class="q-card__section q-card__section--vert"
                              >
                                <q-item-section
                                  avatar
                                  style="margin-bottom: 10px"
                                >
                                  <q-icon
                                    color="secondary"
                                    name="content_copy"
                                  />
                                </q-item-section>
                                <p>Grab your link to share with customers</p>
                              </div>
                            </div>
                          </div>

                          <div class="col-4">
                            <div class="q-card my-card">
                              <div
                                @click="
                                  $refs.stepper.goTo(3);
                                  $router.replace('#top');
                                "
                                class="q-card__section q-card__section--vert"
                              >
                                <q-item-section
                                  avatar
                                  style="margin-bottom: 10px"
                                >
                                  <q-icon color="secondary" name="call" />
                                </q-item-section>
                                <p>Book a call with a contractor adviser</p>
                              </div>
                            </div>
                          </div>
                          <div class="col-4">
                            <div class="q-card my-card">
                              <div
                                @click="
                                  $refs.stepper.goTo(5);
                                  $router.replace('#top');
                                "
                                class="q-card__section q-card__section--vert"
                              >
                                <q-item-section
                                  avatar
                                  style="margin-bottom: 10px"
                                >
                                  <q-icon color="secondary" name="groups" />
                                </q-item-section>
                                <p>Learn how to talk about financing</p>
                              </div>
                            </div>
                          </div>
                          <div class="col-4">
                            <div class="q-card my-card">
                              <div
                                @click="
                                  $refs.stepper.goTo(4);
                                  $router.replace('#top');
                                "
                                class="q-card__section q-card__section--vert"
                              >
                                <q-item-section
                                  avatar
                                  style="margin-bottom: 10px"
                                >
                                  <q-icon
                                    color="secondary"
                                    name="description"
                                  />
                                </q-item-section>
                                <p>See what your customer sees</p>
                              </div>
                            </div>
                          </div>
                          <div class="col-4">
                            <div class="q-card my-card">
                              <div
                                @click="
                                  $refs.stepper.goTo(6);
                                  $router.replace('#top');
                                "
                                class="q-card__section q-card__section--vert"
                              >
                                <q-item-section
                                  avatar
                                  style="margin-bottom: 10px"
                                >
                                  <q-icon color="secondary" name="notes" />
                                </q-item-section>
                                <p>Snag a cheatsheet to answer questions</p>
                              </div>
                            </div>
                          </div>
                          <div class="col-4">
                            <div class="q-card my-card">
                              <div
                                @click="
                                  $refs.stepper.goTo(6);
                                  $router.replace('#top');
                                "
                                class="q-card__section q-card__section--vert"
                              >
                                <q-item-section
                                  avatar
                                  style="margin-bottom: 10px"
                                >
                                  <q-icon color="secondary" name="computer" />
                                </q-item-section>
                                <p>Access your financing portal</p>
                              </div>
                            </div>
                          </div>
                        </div>
                          <br />
                          <br />
                          <br />
                          <br />
                      </div>

                      <div class="showMobile">
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
                            <br />
                            <br />
                            <br />
                            <br />
                            
                      </div>
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

                        <br />
                        
                  
                
                           
                              <div class="q-gutter-y-md">
                         
                                  <q-tabs
                                    v-model="tab"
                                    dense
                                    class="text-grey"
                                    active-color="primary"
                                    indicator-color="primary"
                                    align="justify"
                                    narrow-indicator
                                  >
                                    <q-tab name="text" icon="sms" label="Text" />
                                    <q-tab name="email" icon="outgoing_mail" label="Email" />
                                    <q-tab name="copy" icon="content_copy" label="Copy" />
                                  </q-tabs>

                                  <q-separator />

                                  <q-tab-panels v-model="tab" animated>
                                    <q-tab-panel name="text">
                                      <div class="text-h6">Send me a text</div>
                                     <p> We'll send you a text message of your application link to <br /> <b>555-555-5555</b> </p>
                                     <q-btn
                                        outline
                                        color="accent"
                                        label="Send me a text"
                                        icon-right="navigate_next"
                                        @click="
                                          $router.replace('#top');
                                        "
                                      />
                                    </q-tab-panel>

                                    <q-tab-panel name="email">
                                     <div class="text-h6">Send me an email</div>
                                     <p> We'll send you an email of your application link to <br /> <b>jsample@gmail.com</b> </p>
                                     <q-btn
                                        outline
                                        color="accent"
                                        label="Send me an email"
                                        icon-right="navigate_next"
                                        @click="
                                          $router.replace('#top');
                                        "
                                      />
                                    </q-tab-panel>

                                    <q-tab-panel name="copy">
                                       <div class="text-h6">Copy and paste your link</div>
                                     <p>Copy and paste the link below to send to one of you customers.</p>
                                    <q-input
                                        flat
                                        v-model="text"
                                        placeholder="acornfinance.com/apply/EWY"
                                        text="acornfinance.com/apply/EWY"
                                      >
                                        <template v-slot:append>
                                          <q-icon name="file_copy" color="accent" />
                                        </template>
                                      </q-input>
                                    </q-tab-panel>
                                  </q-tab-panels>
                          

                               
                              </div>
                  
          






             
                

          



                       

                      <br />
                    
                      </q-banner>
                      <br />
                     

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
                        height="900"
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
                    <br/>
                    <br />
                    <br />

                    <template v-slot:navigation>
                   
                      <q-stepper-navigation class="onboarding-experience-navigation">
                        <div style="float: right">
                          <q-btn
                            v-if="step > 1"
                            flat
                            color="secondary"
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
                            color="secondary"
                            :label="step === 6 ? 'My Portal' : 'Next'"
                          ></q-btn>
                        </div>
                        <div style="float: left">
                          <q-btn
                            v-if="step > 1"
                            flat
                            color="secondary"
                            @click="
                              $refs.stepper.goTo(1);
                              $router.replace('#top');
                            "
                            label="Menu"
                            class="q-ml-sm"
                          ></q-btn>
                        </div>
                      </q-stepper-navigation>
                     
                    </template>
                  </q-stepper>

                  <q-dialog v-model="card">
                    <q-card class="my-card">
                      <q-img src="src/assets/welcome-image.png" />

                      <q-card-section>
                        <div
                          class="row no-wrap items-center"
                          style="text-align: center"
                        >
                          <div class="col text-h6 ellipsis">
                            Your first step is out of the way.
                          </div>
                        </div>
                      </q-card-section>

                      <q-card-section
                        class="q-pt-none"
                        style="text-align: center"
                      >
                        <div class="text-subtitle1">
                          Next up, we'll guide you through a few key things
                          you'll need to get the most of Acorn Finance.
                        </div>
                      </q-card-section>
                      <q-separator />

                      <q-card-actions align="right">
                        <q-btn
                          v-close-popup
                          color="secondary"
                          label="Explore"
                        />
                      </q-card-actions>
                    </q-card>
                  </q-dialog>
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
      card: ref(true),
      tab: ref('text'),
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
