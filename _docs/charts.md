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

<div class="row">
{% include cards/bars.html title="Projects" data="Server Migration,20,danger|Sales Tracking,40,warning|Payout Details,80,info|Account Setup,100,success" width=12 %}
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
