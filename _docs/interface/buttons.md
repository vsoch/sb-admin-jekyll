---
layout: default
title: Buttons
---

<!-- Begin Page Content -->
<div class="container-fluid">

  <!-- Page Heading -->
  <h1 class="h3 mb-4 text-gray-800">Buttons</h1>

  <div class="row">

    <div class="col-lg-6">

      <!-- Circle Buttons -->
      <div class="card shadow mb-4">
<div class="card-header py-3">
  <h6 class="m-0 font-weight-bold text-primary">Circle Buttons</h6>
</div>
<div class="card-body">
  <p>Use Font Awesome Icons (included with this theme package) along with the circle buttons as shown in the examples below!</p>
  <!-- Circle Buttons (Default) -->
  <div class="mb-2">
    <code>.btn-circle</code>
  </div>
  <a href="#" class="btn btn-primary btn-circle">
    <i class="fab fa-facebook-f"></i>
  </a>
  <a href="#" class="btn btn-success btn-circle">
    <i class="fas fa-check"></i>
  </a>
  <a href="#" class="btn btn-info btn-circle">
    <i class="fas fa-info-circle"></i>
  </a>
  <a href="#" class="btn btn-warning btn-circle">
    <i class="fas fa-exclamation-triangle"></i>
  </a>
  <a href="#" class="btn btn-danger btn-circle">
    <i class="fas fa-trash"></i>
  </a>
  <!-- Circle Buttons (Small) -->
  <div class="mt-4 mb-2">
    <code>.btn-circle .btn-sm</code>
  </div>
  <a href="#" class="btn btn-primary btn-circle btn-sm">
    <i class="fab fa-facebook-f"></i>
  </a>
  <a href="#" class="btn btn-success btn-circle btn-sm">
    <i class="fas fa-check"></i>
  </a>
  <a href="#" class="btn btn-info btn-circle btn-sm">
    <i class="fas fa-info-circle"></i>
  </a>
  <a href="#" class="btn btn-warning btn-circle btn-sm">
    <i class="fas fa-exclamation-triangle"></i>
  </a>
  <a href="#" class="btn btn-danger btn-circle btn-sm">
    <i class="fas fa-trash"></i>
  </a>
  <!-- Circle Buttons (Large) -->
  <div class="mt-4 mb-2">
    <code>.btn-circle .btn-lg</code>
  </div>
  <a href="#" class="btn btn-primary btn-circle btn-lg">
    <i class="fab fa-facebook-f"></i>
  </a>
  <a href="#" class="btn btn-success btn-circle btn-lg">
    <i class="fas fa-check"></i>
  </a>
  <a href="#" class="btn btn-info btn-circle btn-lg">
    <i class="fas fa-info-circle"></i>
  </a>
  <a href="#" class="btn btn-warning btn-circle btn-lg">
    <i class="fas fa-exclamation-triangle"></i>
  </a>
  <a href="#" class="btn btn-danger btn-circle btn-lg">
    <i class="fas fa-trash"></i>
  </a>
</div>
      </div>

      <!-- Brand Buttons -->
      <div class="card shadow mb-4">
<div class="card-header py-3">
  <h6 class="m-0 font-weight-bold text-primary">Brand Buttons</h6>
</div>
<div class="card-body">
  <p>Google and Facebook buttons are available featuring each company's respective brand color. They are used on the user login and registration pages.</p>
  <p>You can create more custom buttons by adding a new color variable in the <code>_variables.scss</code> file and then using the Bootstrap button variant mixin to create a new style, as demonstrated in the <code>_buttons.scss</code> file.</p>
  <a href="#" class="btn btn-google btn-block"><i class="fab fa-google fa-fw"></i> .btn-google</a>
  <a href="#" class="btn btn-facebook btn-block"><i class="fab fa-facebook-f fa-fw"></i> .btn-facebook</a>

</div>
      </div>

    </div>

    <div class="col-lg-6">

      <div class="card shadow mb-4">
<div class="card-header py-3">
  <h6 class="m-0 font-weight-bold text-primary">Split Buttons with Icon</h6>
</div>
<div class="card-body">
  <p>Works with any button colors, just use the <code>.btn-icon-split</code> class and the markup in the examples below. The examples below also use the <code>.text-white-50</code> helper class on the icons for additional styling, but it is not required.</p>

  {% include buttons/split-button.html style="primary" title="Split Button Primary" icon="fa-flag"%}
  <div class="my-2"></div>
  {% include buttons/split-button.html style="success" title="Split Button Success" icon="fa-check"%}
  <div class="my-2"></div>
  {% include buttons/split-button.html style="info" title="Split Button Info" icon="fa-info-circle"%}
  <div class="my-2"></div>
  {% include buttons/split-button.html style="warning" title="Split Button Warning" icon="fa-exclamation-triangle"%}
  <div class="my-2"></div>
  {% include buttons/split-button.html style="danger" title="Split Button Danger" icon="fa-trash"%}
  <div class="my-2"></div>
  {% include buttons/split-button.html style="secondary" title="Split Button Secondary" icon="fa-arrow-right"%}
  <div class="my-2"></div>
  {% include buttons/split-button.html style="light" title="Split Button Primary" icon="fa-arrow-right"%}
  <div class="mb-4"></div>

  <p>Also works with small and large button classes!</p>
  <a href="#" class="btn btn-primary btn-icon-split btn-sm">
    <span class="icon text-white-50">
      <i class="fas fa-flag"></i>
    </span>
    <span class="text">Split Button Small</span>
  </a>
  <div class="my-2"></div>
  <a href="#" class="btn btn-primary btn-icon-split btn-lg">
    <span class="icon text-white-50">
      <i class="fas fa-flag"></i>
    </span>
    <span class="text">Split Button Large</span>
  </a>
</div>
      </div>

    </div>

  </div>
