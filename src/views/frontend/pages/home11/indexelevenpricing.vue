<template>
  <!-- Pricing Plan -->
  <div class="pricing-section-sixteen">
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <div class="section-header-sixteen text-center">
            <p>OUr services</p>
            <h2>Featured Services</h2>
          </div>
        </div>
      </div>
      <div class="row justify-content-center align-items-center">
        <div class="col-lg-4 col-sm-12 aos" data-aos="fade-up">
          <div class="card pricing-card">
            <div class="card-body">
              <div class="pricing-header">
                <div class="pricing-header-info">
                  <div class="pricing-icon">
                    <span>
                      <img src="@/assets/img/icons/price-icon1.svg" alt="icon" />
                    </span>
                  </div>
                  <div class="pricing-title">
                    <p>For individuals</p>
                    <h4>Basic</h4>
                  </div>
                </div>
                <div class="pricing-header-text">
                  <p>
                    Lorem ipsum dolor consectetur adipiscing elit,sed do eiusmod tempor
                  </p>
                </div>
              </div>
              <div class="pricing-info">
                <div class="pricing-amount">
                  <h2>$99 <span>/monthly</span></h2>
                  <h6>What’s included</h6>
                </div>
                <div class="pricing-list">
                  <ul>
                    <li>Lorem ipsum dolor amet, consectetur</li>
                    <li>Lorem ipsum amet, consectetur</li>
                    <li>Lorem ipsum dolor amet, consectetur</li>
                    <li>Lorem ipsum amet, consectetur</li>
                  </ul>
                </div>
                <div class="pricing-btn">
                  <router-link to="/pricing" class="btn">Choose Plan</router-link>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="col-lg-4 col-sm-12 aos" data-aos="fade-up">
          <div class="card pricing-card pricing-card-active">
            <div class="card-body">
              <div class="pricing-header">
                <div class="pricing-header-info">
                  <div class="pricing-icon">
                    <span>
                      <img src="@/assets/img/icons/price-icon2.svg" alt="icon" />
                    </span>
                  </div>
                  <div class="pricing-title">
                    <p>For startups</p>
                    <h4>Pro</h4>
                  </div>
                  <div class="pricing-tag">
                    <span>Popular</span>
                  </div>
                </div>
                <div class="pricing-header-text">
                  <p>
                    Lorem ipsum dolor consectetur adipiscing elit,sed do eiusmod tempor
                  </p>
                </div>
              </div>
              <div class="pricing-info">
                <div class="pricing-amount">
                  <h2>$199 <span>/monthly</span></h2>
                  <h6>What’s included</h6>
                </div>
                <div class="pricing-list">
                  <ul>
                    <li>Lorem ipsum dolor amet, consectetur</li>
                    <li>Lorem ipsum amet, consectetur</li>
                    <li>Neque porro quisquam est, qui dolorem</li>
                    <li>Lorem ipsum dolor amet, consectetur</li>
                    <li>Lorem ipsum amet, consectetur</li>
                    <li>Sed ut perspiciatis unde</li>
                    <li>Nemo enim ipsam voluptatem</li>
                  </ul>
                </div>
                <div class="pricing-btn">
                  <router-link to="/pricing" class="btn">Choose Plan</router-link>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="col-lg-4 col-sm-12 aos" data-aos="fade-up">
          <div class="card pricing-card">
            <div class="card-body">
              <div class="pricing-header">
                <div class="pricing-header-info">
                  <div class="pricing-icon">
                    <span>
                      <img src="@/assets/img/icons/price-icon3.svg" alt="icon" />
                    </span>
                  </div>
                  <div class="pricing-title">
                    <p>For big companies</p>
                    <h4>Enterprise</h4>
                  </div>
                </div>
                <div class="pricing-header-text">
                  <p>
                    Lorem ipsum dolor consectetur adipiscing elit,sed do eiusmod tempor
                  </p>
                </div>
              </div>
              <div class="pricing-info">
                <div class="pricing-amount">
                  <h2>$399 <span>/monthly</span></h2>
                  <h6>What’s included</h6>
                </div>
                <div class="pricing-list">
                  <ul>
                    <li>Lorem ipsum dolor amet, consectetur</li>
                    <li>Lorem ipsum amet, consectetur</li>
                    <li>Lorem ipsum dolor amet, consectetur</li>
                    <li>Lorem ipsum amet, consectetur</li>
                  </ul>
                </div>
                <div class="pricing-btn">
                  <router-link to="/pricing" class="btn">Choose Plan</router-link>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <!-- /Pricing Plan -->
</template>
<script>
import AOS from "aos";
import "aos/dist/aos.css";
export default {
  mounted() {
    this.$nextTick(() => {
      AOS.init();
    });
  },
};
</script>
