---
layout: default
title: Charts
---

<h1 class="h3 mb-2 text-gray-800">Charts</h1>
<p class="mb-4">Chart.js is a third party plugin that is used to generate the charts in this theme. The charts below have been customized - for further customization options, please visit the <a target="_blank" href="https://www.chartjs.org/docs/latest/">official Chart.js documentation</a>.</p>

<!-- Example Cards -->

<div class="row">

{% include cards/statistic.html icon="fa-calendar" value="$40,000" title="Earnings (Monthly)" style="primary" %}
{% include cards/statistic.html icon="fa-dollar-sign" value="$215,000" title="Earnings (Annual)" style="success" %}
{% include cards/progress.html title="Tasks" icon="fa-clipboard-list" percent="50" %}
{% include cards/statistic.html icon="fa-comments" value="18" title="Pending Requests" style="warning" %}

</div>

<!-- Example Charts -->

<div class="row">
{% include charts/area.html width=8 labels="Jan,Feb,Mar,Apr,May,Jun,Jul,Aug,Sep,Oct,Nov,Dec" title="Candy Sales" datasets="Earnings:0,10000,5000,15000,10000,20000,15000,25000,20000,30000,25000,40000" currency='true' %}
{% include charts/pie.html data="55,30,15" width=4 title="Candy Breakdown" labels="Snickers,Twix,Reeses" %}
</div>

<div class="row">
{% include charts/bar.html title="Total Revenue" width=12 labels="January,February,March,April,May,June" datasets="Revenue:4215,5312,6251,7841,9821,14984," currency="true" %}
</div>

<!-- Content Row -->
<div class="row">

  <!-- Content Column -->
  <div class="col-lg-6 mb-4">

    <!-- Project Card Example -->
    <div class="card shadow mb-4">
      <div class="card-header py-3">
        <h6 class="m-0 font-weight-bold text-primary">Projects</h6>
      </div>
      <div class="card-body">
        <h4 class="small font-weight-bold">Server Migration <span class="float-right">20%</span></h4>
        <div class="progress mb-4">
<div class="progress-bar bg-danger" role="progressbar" style="width: 20%" aria-valuenow="20" aria-valuemin="0" aria-valuemax="100"></div>
        </div>
        <h4 class="small font-weight-bold">Sales Tracking <span class="float-right">40%</span></h4>
        <div class="progress mb-4">
<div class="progress-bar bg-warning" role="progressbar" style="width: 40%" aria-valuenow="40" aria-valuemin="0" aria-valuemax="100"></div>
        </div>
        <h4 class="small font-weight-bold">Customer Database <span class="float-right">60%</span></h4>
        <div class="progress mb-4">
<div class="progress-bar" role="progressbar" style="width: 60%" aria-valuenow="60" aria-valuemin="0" aria-valuemax="100"></div>
        </div>
        <h4 class="small font-weight-bold">Payout Details <span class="float-right">80%</span></h4>
        <div class="progress mb-4">
<div class="progress-bar bg-info" role="progressbar" style="width: 80%" aria-valuenow="80" aria-valuemin="0" aria-valuemax="100"></div>
        </div>
        <h4 class="small font-weight-bold">Account Setup <span class="float-right">Complete!</span></h4>
        <div class="progress">
<div class="progress-bar bg-success" role="progressbar" style="width: 100%" aria-valuenow="100" aria-valuemin="0" aria-valuemax="100"></div>
        </div>
      </div>
    </div>

    <!-- Color System -->
    <div class="row">
      <div class="col-lg-6 mb-4">
        <div class="card bg-primary text-white shadow">
<div class="card-body">
  Primary
  <div class="text-white-50 small">#4e73df</div>
</div>
        </div>
      </div>
      <div class="col-lg-6 mb-4">
        <div class="card bg-success text-white shadow">
<div class="card-body">
  Success
  <div class="text-white-50 small">#1cc88a</div>
</div>
        </div>
      </div>
      <div class="col-lg-6 mb-4">
        <div class="card bg-info text-white shadow">
<div class="card-body">
  Info
  <div class="text-white-50 small">#36b9cc</div>
</div>
        </div>
      </div>
      <div class="col-lg-6 mb-4">
        <div class="card bg-warning text-white shadow">
<div class="card-body">
  Warning
  <div class="text-white-50 small">#f6c23e</div>
</div>
        </div>
      </div>
      <div class="col-lg-6 mb-4">
        <div class="card bg-danger text-white shadow">
<div class="card-body">
  Danger
  <div class="text-white-50 small">#e74a3b</div>
</div>
        </div>
      </div>
      <div class="col-lg-6 mb-4">
        <div class="card bg-secondary text-white shadow">
<div class="card-body">
  Secondary
  <div class="text-white-50 small">#858796</div>
</div>
        </div>
      </div>
    </div>

  </div>

  <div class="col-lg-6 mb-4">

    <!-- Illustrations -->
    <div class="card shadow mb-4">
      <div class="card-header py-3">
        <h6 class="m-0 font-weight-bold text-primary">Illustrations</h6>
      </div>
      <div class="card-body">
        <div class="text-center">
<img class="img-fluid px-3 px-sm-4 mt-3 mb-4" style="width: 25rem;" src="{{ site.url }}{{ site.baseurl }}/assets/img/undraw_posting_photo.svg" alt="">
        </div>
        <p>Add some quality, svg illustrations to your project courtesy of <a target="_blank" rel="nofollow" href="https://undraw.co/">unDraw</a>, a constantly updated collection of beautiful svg images that you can use completely free and without attribution!</p>
        <a target="_blank" rel="nofollow" href="https://undraw.co/">Browse Illustrations on unDraw &rarr;</a>
      </div>
    </div>

    <!-- Approach -->
    <div class="card shadow mb-4">
      <div class="card-header py-3">
        <h6 class="m-0 font-weight-bold text-primary">Development Approach</h6>
      </div>
      <div class="card-body">
        <p>SB Admin 2 makes extensive use of Bootstrap 4 utility classes in order to reduce CSS bloat and poor page performance. Custom CSS classes are used to create custom components and custom utility classes.</p>
        <p class="mb-0">Before working with this theme, you should become familiar with the Bootstrap framework, especially the utility classes.</p>
      </div>
    </div>

  </div>
</div>
