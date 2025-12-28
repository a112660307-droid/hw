<!doctype html>
<html lang="zh-TW">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>作業首頁｜Bootstrap + 新聞展示 + BMI</title>

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
              <a class="nav-link" href="#news">新聞</a>
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
            <!-- 若你有 images/photo1.png，可改回：images/photo1.png -->
            <img src="https://picsum.photos/seed/firstslide/1400/600?v=3" class="d-block w-100" alt="first slide">
            <div class="carousel-caption d-none d-md-block">
              <h5>Bootstrap 作業展示</h5>
              <p>Carousel + Accordion + Cards + BMI 計算器</p>
            </div>
          </div>

          <div class="carousel-item">
            <img src="https://picsum.photos/seed/firstslide/1400/600" class="d-block w-100" alt="first slide">
            <div class="carousel-caption d-none d-md-block">
              <h5>新聞卡片區</h5>
              <p></p>
            </div>
          </div>

          <div class="carousel-item">
            <img src="https://images.unsplash.com/photo-1451187580459-43490279c0fa?auto=format&fit=crop&w=1400&q=60" class="d-block w-100" alt="third slide">
            <div class="carousel-caption d-none d-md-block">
              <h5>互動功能</h5>
              <p>JavaScript：BMI 計算與結果判定</p>
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

      <!-- 上半部：注意事項 + BMI -->
      <div class="row text-start mt-4">
        <div class="col-sm-8">
          <h1 class="h3">注意事項</h1>

          <div class="accordion" id="accordionExample">
            <div class="accordion-item">
              <h2 class="accordion-header">
                <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                  這份作業用到的 Bootstrap 元件
                </button>
              </h2>
              <div id="collapseOne" class="accordion-collapse collapse show" data-bs-parent="#accordionExample">
                <div class="accordion-body">
                  <ul class="mb-0">
                    <li>Navbar：頁面導覽（首頁 / 履歷 / 新聞 / BMI）</li>
                    <li>Carousel：輪播圖</li>
                    <li>Accordion：可收合區塊</li>
                    <li>Card：新聞展示卡片</li>
                    <li>Grid：row / col 版面配置</li>
                  </ul>
                </div>
              </div>
            </div>

            <div class="accordion-item">
              <h2 class="accordion-header">
                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
                  互動功能（JavaScript）
                </button>
              </h2>
              <div id="collapseTwo" class="accordion-collapse collapse" data-bs-parent="#accordionExample">
                <div class="accordion-body">
                  使用者輸入身高與體重，按下按鈕後會計算 BMI 並顯示判定結果（過輕/正常/過重/肥胖）。
                </div>
              </div>
            </div>

            <div class="accordion-item">
              <h2 class="accordion-header">
                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
                  新聞展示區說明
                </button>
              </h2>
              <div id="collapseThree" class="accordion-collapse collapse" data-bs-parent="#accordionExample">
                <div class="accordion-body">
                </div>
              </div>
            </div>
          </div>
        </div>

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

            <button class="btn btn-primary w-100" onclick="calculateBMI()">計算 BMI</button>
          </div>
        </div>
      </div>

      <!-- 簡單 Grid -->
      <div class="row mt-4">
        <div class="col-2 p-3 mb-2 bg-primary text-white">col</div>
        <div class="col-8 p-3 mb-2 bg-secondary text-white">col</div>
        <div class="col-2 p-3 mb-2 bg-success text-white">col</div>
      </div>

      <!-- 新聞區 -->
      <div class="text-start mt-4" id="news">
        <h2 class="h3">近期時事新聞展示</h2>
        <p class="text-secondary mb-3"></p>

        <div class="row justify-content-center">
          <!-- 1 -->
          <div class="col-12 col-md-6 col-lg-4 mb-4">
            <div class="card h-100 shadow-sm">
              <img src="https://images.unsplash.com/photo-1529101091764-c3526daf38fe?auto=format&fit=crop&w=900&q=60" class="card-img-top" alt="news1">
              <div class="card-body">
                <h5 class="card-title">中國宣布制裁多家美國國防公司（涉對台軍售）</h5>
                <p class="card-text">報導指出，中國針對多家美國國防相關公司與部分高層宣布制裁措施，背景是近期對台軍售爭議。</p>
                <a href="https://apnews.com/article/31e1bdef85a4cae9a765b189497ca3bf" class="btn btn-primary" target="_blank" rel="noopener">閱讀更多（AP）</a>
              </div>
            </div>
          </div>

          <!-- 2 -->
          <div class="col-12 col-md-6 col-lg-4 mb-4">
            <div class="card h-100 shadow-sm">
              <img src="https://images.unsplash.com/photo-1520607162513-77705c0f0d4a?auto=format&fit=crop&w=900&q=60" class="card-img-top" alt="news2">
              <div class="card-body">
                <h5 class="card-title">日本提出創紀錄預算，並試圖控制新增債務</h5>
                <p class="card-text">Reuters 報導提到，日本提出規模創高的新年度預算，同時把新增發債控制在一定水位，以兼顧刺激與財政壓力。</p>
                <a href="https://www.reuters.com/world/asia-pacific/core-inflation-japans-capital-slows-december-stays-above-boj-target-2025-12-25/" class="btn btn-primary" target="_blank" rel="noopener">閱讀更多（Reuters）</a>
              </div>
            </div>
          </div>

          <!-- 3 -->
          <div class="col-12 col-md-6 col-lg-4 mb-4">
            <div class="card h-100 shadow-sm">
              <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?auto=format&fit=crop&w=900&q=60" class="card-img-top" alt="news3">
              <div class="card-body">
                <h5 class="card-title">台灣 2025 經濟成長預測：AI 需求帶動</h5>
                <p class="card-text">Focus Taiwan（CNA）報導提到，研究機構預估台灣 2025 經濟成長，與全球 AI 需求強勁有關。</p>
                <a href="https://focustaiwan.tw/business/202512220012" class="btn btn-primary" target="_blank" rel="noopener">閱讀更多（CNA）</a>
              </div>
            </div>
          </div>

          <!-- 4 -->
          <div class="col-12 col-md-6 col-lg-4 mb-4">
            <div class="card h-100 shadow-sm">
              <img src="https://images.unsplash.com/photo-1550751827-4bd374c3f58b?auto=format&fit=crop&w=900&q=60" class="card-img-top" alt="news4">
              <div class="card-body">
                <h5 class="card-title">美國發布 AI 國家政策框架相關行政命令</h5>
                <p class="card-text">白宮網站公布行政命令，內容聚焦 AI 政策框架與跨州規範一致性等議題。</p>
                <a href="https://www.whitehouse.gov/presidential-actions/2025/12/eliminating-state-law-obstruction-of-national-artificial-intelligence-policy/" class="btn btn-primary" target="_blank" rel="noopener">閱讀更多（White House）</a>
              </div>
            </div>
          </div>

          <!-- 5 -->
          <div class="col-12 col-md-6 col-lg-4 mb-4">
            <div class="card h-100 shadow-sm">
              <img src="https://images.unsplash.com/photo-1526304640581-d334cdbbf45e?auto=format&fit=crop&w=900&q=60" class="card-img-top" alt="news5">
              <div class="card-body">
                <h5 class="card-title">聯準會發布 12 月 FOMC 聲明</h5>
                <p class="card-text">Federal Reserve 官網公告最新 FOMC 聲明，內容聚焦最大就業與通膨目標，以及對經濟前景不確定性的評估。</p>
                <a href="https://www.federalreserve.gov/newsevents/pressreleases/monetary20251210a.htm" class="btn btn-primary" target="_blank" rel="noopener">閱讀更多（Fed）</a>
              </div>
            </div>
          </div>

          <!-- 6 -->
          <div class="col-12 col-md-6 col-lg-4 mb-4">
            <div class="card h-100 shadow-sm">
              <img src="https://images.unsplash.com/photo-1521540216272-a50305cd4421?auto=format&fit=crop&w=900&q=60" class="card-img-top" alt="news6">
              <div class="card-body">
                <h5 class="card-title">2025 年多國央行降息速度加快（Reuters 分析）</h5>
                <p class="card-text">Reuters 報導整理指出，2025 年多國央行的降息節奏與規模，呈現出較明顯的寬鬆趨勢。</p>
                <a href="https://www.reuters.com/world/europe/major-central-banks-deliver-biggest-easing-push-over-decade-2025-2025-12-23/" class="btn btn-primary" target="_blank" rel="noopener">閱讀更多（Reuters）</a>
              </div>
            </div>
          </div>
        </div>
      </div>

      <footer class="py-4 text-center text-secondary">
        <small>© 2025 作業練習｜Bootstrap + 新聞卡片 + BMI</small>
      </footer>
    </div>
  </body>
</html>
