<!doctype html>
<html lang="zh-TW">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>作業首頁｜Bootstrap + BMI</title>

    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-sRIl4kxILFvY47J16cr9ZwB07vP4J8+LH7qKQnuqkuIAvNWLzeN8tE5YBujZqJLB" crossorigin="anonymous">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/js/bootstrap.bundle.min.js" integrity="sha384-FKyoEForCGlyvwx9Hj09JcYn3nv7wiPVlz7YYwJrWVcXK/BmnVDxM+D2scQbITxI" crossorigin="anonymous"></script>

    <script>
      function calculateBMI() {
        let height = document.getElementById("height").value;
        let weight = document.getElementById("weight").value;

        if (height === "" || weight === "") {
          alert("請輸入身高和體重！");
          return;
        }

        height = height / 100; // cm -> m
        let bmi = weight / (height * height);
        bmi = bmi.toFixed(2);

        let result = "";
        if (bmi < 18.5) result = "體重過輕";
        else if (bmi < 24) result = "正常範圍";
        else if (bmi < 27) result = "過重";
        else result = "肥胖";

        alert("你的 BMI 是：" + bmi + "\n判定結果：" + result);
      }
    </script>
  </head>

  <body>
    <!-- Navbar -->
    <nav class="navbar navbar-expand-lg bg-body-tertiary">
      <div class="container">
        <a class="navbar-brand" href="index.html">
          <img src="https://img-s-msn-com.akamaized.net/tenant/amp/entityid/AA1RO7tG.img?w=268&h=140&q=60&m=6&f=jpg&u=t" alt="Logo" width="30" height="24" class="d-inline-block align-text-top">
          ABOUT ME
        </a>

        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>

        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav">
            <li class="nav-item">
              <a class="nav-link active" aria-current="page" href="index.html">首頁</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="resume.html">履歷</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#bmi">BMI</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <div class="container text-center my-4">

      <!-- Carousel -->
      <div id="carouselExampleCaptions" class="carousel slide" data-bs-ride="carousel">
        <div class="carousel-indicators">
          <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
          <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="1" aria-label="Slide 2"></button>
          <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="2" aria-label="Slide 3"></button>
        </div>

        <div class="carousel-inner">
          <div class="carousel-item active">
            <!-- 如果你有 images/photo1.png，可改回去；沒有就先用外部圖避免破圖 -->
            <img src="https://images.unsplash.com/photo-1520975958225-5f61f0f8a1a8?auto=format&fit=crop&w=1200&q=60" class="d-block w-100" alt="first slide">
            <div class="carousel-caption d-none d-md-block">
              <h5>Welcome</h5>
              <p>作業首頁：Bootstrap 元件練習</p>
            </div>
          </div>

          <div class="carousel-item">
            <img src="https://images.unsplash.com/photo-1517248135467-4c7edcad34c4?auto=format&fit=crop&w=1200&q=60" class="d-block w-100" alt="second slide">
            <div class="carousel-caption d-none d-md-block">
              <h5>Components</h5>
              <p>Carousel / Accordion / Card / Grid</p>
            </div>
          </div>

          <div class="carousel-item">
            <img src="https://img-s-msn-com.akamaized.net/tenant/amp/entityid/AA1K4UpQ.img?w=268&h=140&q=60&m=6&f=jpg&u=t" class="d-block w-100" alt="third slide">
            <div class="carousel-caption d-none d-md-block">
              <h5>Practice</h5>
              <p>加入簡單互動：BMI 計算</p>
            </div>
          </div>
        </div>

        <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide="prev">
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide="next">
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Next</span>
        </button>
      </div>

      <div class="row text-start mt-4">
        <!-- Left -->
        <div class="col-sm-8">
          <h1 class="h3">注意事項</h1>

          <div class="accordion" id="accordionExample">
            <div class="accordion-item">
              <h2 class="accordion-header">
                <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                  Accordion Item #1
                </button>
              </h2>
              <div id="collapseOne" class="accordion-collapse collapse show" data-bs-parent="#accordionExample">
                <div class="accordion-body">
                  <strong>這是第一個區塊。</strong> 你可以在這裡放作業說明、使用到的 Bootstrap 元件清單等內容。
                </div>
              </div>
            </div>

            <div class="accordion-item">
              <h2 class="accordion-header">
                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
                  Accordion Item #2
                </button>
              </h2>
              <div id="collapseTwo" class="accordion-collapse collapse" data-bs-parent="#accordionExample">
                <div class="accordion-body">
                  <strong>這是第二個區塊。</strong> 可以寫你做了哪些功能：輪播、手風琴、卡片、BMI 計算器。
                </div>
              </div>
            </div>

            <div class="accordion-item">
              <h2 class="accordion-header">
                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
                  Accordion Item #3（卡片示範）
                </button>
              </h2>
              <div id="collapseThree" class="accordion-collapse collapse" data-bs-parent="#accordionExample">
                <div class="accordion-body">
                  <div class="card" style="max-width: 520px;">
                    <img src="https://img-s-msn-com.akamaized.net/tenant/amp/entityid/AA1SKKR2.img?w=268&h=140&q=60&m=6&f=jpg&x=821&y=224&u=t" class="card-img-top" alt="card image">
                    <div class="card-body">
                      <h5 class="card-title">Card 範例</h5>
                      <p class="card-text">這裡示範 Bootstrap Card 元件，可以放新聞摘要、作品介紹或活動簡介。</p>
                      <a href="https://reurl.cc/rKkEyy" class="btn btn-primary">connect</a>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Right: BMI -->
        <div class="col-sm-4" id="bmi">
          <h1 class="h3">BMI</h1>

          <div class="card shadow p-4">
            <h2 class="h5 text-center mb-4">BMI 計算器</h2>

            <div class="mb-3">
              <label class="form-label">身高（公分）</label>
              <input type="number" id="height" class="form-control" placeholder="例如：170">
            </div>

            <div class="mb-3">
              <label class="form-label">體重（公斤）</label>
              <input type="number" id="weight" class="form-control" placeholder="例如：60">
            </div>

            <button class="btn btn-primary w-100" onclick="calculateBMI()">
              計算 BMI
            </button>
          </div>
        </div>
      </div>

      <!-- simple grid row -->
      <div class="row mt-4">
        <div class="col-2 p-3 mb-2 bg-primary text-white">col</div>
        <div class="col-8 p-3 mb-2 bg-secondary text-white">col</div>
        <div class="col-2 p-3 mb-2 bg-success text-white">col</div>
      </div>

      <!-- cards -->
      <div class="row justify-content-center mt-3">
        <div class="col-12 col-md-6 col-lg-3 p-3 mb-2 bg-primary text-white">
          <div class="card text-dark" style="width: 18rem;">
            <img src="https://img-s-msn-com.akamaized.net/tenant/amp/entityid/AA1SKKR2.img?w=268&h=140&q=60&m=6&f=jpg&x=821&y=224&u=t" class="card-img-top" alt="...">
            <div class="card-body">
              <h5 class="card-title">作品/文章</h5>
              <p class="card-text">你可以把這裡當作作品卡片區，放連結與簡介。</p>
              <a href="https://reurl.cc/rKkEyy" class="btn btn-primary">connect</a>
            </div>
          </div>
        </div>

        <div class="col-12 col-md-6 col-lg-3 p-3 mb-2 bg-secondary text-white">
          <div class="card text-dark" style="width: 18rem;">
            <img src="https://img-s-msn-com.akamaized.net/tenant/amp/entityid/AA1SNnlR.img?w=268&h=140&q=60&m=6&f=jpg&u=t" class="card-img-top" alt="...">
            <div class="card-body">
              <h5 class="card-title">Card title</h5>
              <p class="card-text">Some quick example text to build on the card title.</p>
              <a href="#" class="btn btn-primary">Go somewhere</a>
            </div>
          </div>
        </div>

        <div class="col-12 col-md-6 col-lg-3 p-3 mb-2 bg-success text-white">
          <div class="card text-dark" style="width: 18rem;">
            <img src="https://images.unsplash.com/photo-1522071820081-009f0129c71c?auto=format&fit=crop&w=900&q=60" class="card-img-top" alt="...">
            <div class="card-body">
              <h5 class="card-title">Card title</h5>
              <p class="card-text">把 src="..." 改成圖片網址後，就不會破圖。</p>
              <a href="#" class="btn btn-primary">Go somewhere</a>
            </div>
          </div>
        </div>

        <div class="col-12 col-md-6 col-lg-3 p-3 mb-2 bg-warning text-white">
          <div class="card text-dark" style="width: 18rem;">
            <img src="https://images.unsplash.com/photo-1522202176988-66273c2fd55f?auto=format&fit=crop&w=900&q=60" class="card-img-top" alt="...">
            <div class="card-body">
              <h5 class="card-title">Card title</h5>
              <p class="card-text">這張卡片也改成正常圖片。</p>
              <a href="#" class="btn btn-primary">Go somewhere</a>
            </div>
          </div>
        </div>
      </div>

      <footer class="py-4 text-center text-secondary">
        <small>© 2025 作業練習｜Bootstrap + BMI</small>
      </footer>
    </div>
  </body>
</html>
