<template>
  <!-- Main Wrapper -->
  <div class="main-wrapper">
    <layoutheader></layoutheader>
    <breadcrumb1 :title="title" :text="text" :text1="text1" />

    <!-- Page Content -->
    <div class="content">
      <div class="container">
        <div class="row">
          <div class="col-md-5 col-lg-4 col-xl-3 theiaStickySidebar">
            <div class="stickysidebar">
              <profilewidget />
            </div>
          </div>
          <div class="col-md-7 col-lg-8 col-xl-9">
            <div class="card">
              <div class="card-header">
                <h4 class="card-title mb-0">Edit Billing</h4>
              </div>
              <div class="card-body">
                <div class="row">
                  <div class="col-sm-6">
                    <div class="biller-info">
                      <h4 class="d-block">Dr. Darren Elder</h4>
                      <span class="d-block text-sm text-muted">Dentist</span>
                      <span class="d-block text-sm text-muted"
                        >Newyork, United States</span
                      >
                    </div>
                  </div>
                  <div class="col-sm-6 text-sm-end">
                    <div class="billing-info">
                      <h4 class="d-block">1 November 2023</h4>
                      <span class="d-block text-muted">#INV0001</span>
                    </div>
                  </div>
                </div>

                <!-- Add Item -->
                <div class="add-more-item text-end">
                  <a href="javascript:void(0);" @click="addItem"
                    ><i class="fas fa-plus-circle"></i> Add Item</a
                  >
                </div>
                <!-- /Add Item -->

                <!-- Billing Item -->
                <div class="card card-table">
                  <div class="card-body">
                    <div class="table-responsive">
                      <table class="table table-hover table-center">
                        <thead>
                          <tr>
                            <th>Title</th>
                            <th>Amount</th>
                            <th class="custom-class"></th>
                          </tr>
                        </thead>
                        <tbody>
                          <tr v-for="(item, index) in services" :key="index">
                            <td>
                              <input
                                type="text"
                                class="form-control"
                                v-model="item.service"
                              />
                            </td>
                            <td>
                              <input
                                type="text"
                                class="form-control"
                                v-model="item.fee"
                              />
                            </td>
                            <td>
                              <a
                                href="javascript:void(0)"
                                @click="removeItem(index)"
                                class="btn bg-danger-light trash"
                                ><i class="far fa-trash-alt"></i
                              ></a>
                            </td>
                          </tr>
                        </tbody>
                      </table>
                    </div>
                  </div>
                </div>
                <!-- /Billing Item -->

                <!-- Signature -->
                <div class="row">
                  <div class="col-md-12 text-end">
                    <div class="signature-wrap">
                      <div class="signature">Click here to sign</div>
                      <div class="sign-name">
                        <p class="mb-0">( Dr. Darren Elder )</p>
                        <span class="text-muted">Signature</span>
                      </div>
                    </div>
                  </div>
                </div>
                <!-- /Signature -->

                <!-- Submit Section -->
                <div class="row">
                  <div class="col-md-12">
                    <div class="submit-section">
                      <b-button type="submit" class="btn btn-primary submit-btn">
                        Save
                      </b-button>
                      <b-button type="reset" class="btn btn-secondary submit-btn">
                        Clear
                      </b-button>
                    </div>
                  </div>
                </div>
                <!-- /Submit Section -->
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- /Page Content -->
    <indexfooter></indexfooter>
  </div>
  <!-- /Main Wrapper -->
</template>
<script>
export default {
  data() {
    return {
      title: "Edit Billing",
      text: "Home",
      text1: "Edit Billing",
      services: [
        { service: "Consulting Fee", fee: "$330" },
        { service: "Video Calling Appointment", fee: "$100" },
      ],
    };
  },
  methods: {
    addItem() {
      this.services.push({ service: "", fee: "" });
    },
    removeItem(index) {
      this.services.splice(index, 1);
    },
  },
};
</script>
