<!doctype html>
<html lang="zh-TW">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Bootstrap demo</title>
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

            // 身高轉成公尺
            height = height / 100;

            let bmi = weight / (height * height);
            bmi = bmi.toFixed(2);

            let result = "";

            if (bmi < 18.5) {
                result = "體重過輕";
            } else if (bmi < 24) {
                result = "正常範圍";
            } else if (bmi < 27) {
                result = "過重";
            } else {
                result = "肥胖";
            }

            alert("你的 BMI 是：" + bmi + "\n判定結果：" + result);
        }
    </script>
    
  
  </head>
  <body>
    
      <nav class="navbar navbar-expand-lg bg-body-tertiary">
        <div class="container">

        <a class="navbar-brand" href="page1.html">
          <img src="https://img-s-msn-com.akamaized.net/tenant/amp/entityid/AA1RO7tG.img?w=268&h=140&q=60&m=6&f=jpg&u=t" alt="Logo" width="30" height="24" class="d-inline-block align-text-top">
          ABOUT ME
        </a>          
          
          <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav">
              <li class="nav-item">
                <a class="nav-link active" aria-current="page" href="page2.html">Page2.html</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#">Features</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#">Pricing</a>
              </li>

            </ul>
          </div>
        </div>
      </nav>


    
    <div class="container text-center">
     
      
       <div id="carouselExampleCaptions" class="carousel slide">
        <div class="carousel-indicators">
          <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
          <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="1" aria-label="Slide 2"></button>
          <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="2" aria-label="Slide 3"></button>
        </div>
        <div class="carousel-inner">
          <div class="carousel-item active">
            <img src="images/photo1.png" class="d-block w-100" alt="firs page">
            <div class="carousel-caption d-none d-md-block">
              <h5>First slide label</h5>
              <p>Some representative placeholder content for the first slide.</p>
            </div>
          </div>
          <div class="carousel-item">
            <img src="..." class="d-block w-100" alt="the second photo">
            <div class="carousel-caption d-none d-md-block">
              <h5>Second slide label</h5>
              <p>Some representative placeholder content for the second slide.</p>
            </div>
          </div>
          <div class="carousel-item">
            <img src="https://img-s-msn-com.akamaized.net/tenant/amp/entityid/AA1K4UpQ.img?w=268&h=140&q=60&m=6&f=jpg&u=t" class="d-block w-100" alt="...">
            <div class="carousel-caption d-none d-md-block">
              <h5>Third slide label</h5>
              <p>Some representative placeholder content for the third slide.</p>
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
      
      
      
      
      
      <div class="row">
        <!-- commment -->
        
        <div class="col-sm-8">
          <h1>注意事項:</h1>
          <div class="accordion" id="accordionExample">
            <div class="accordion-item">
              <h2 class="accordion-header">
                <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                  Accordion Item #1
                </button>
              </h2>
              <div id="collapseOne" class="accordion-collapse collapse show" data-bs-parent="#accordionExample">
                <div class="accordion-body">
                  <strong>This is the first item’s accordion body.</strong> It is shown by default, until the collapse plugin adds the appropriate classes that we use to style each element. These classes control the overall appearance, as well as the showing and hiding via CSS transitions. You can modify any of this with custom CSS or overriding our default variables. It’s also worth noting that just about any HTML can go within the <code>.accordion-body</code>, though the transition does limit overflow.
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
                  <strong>This is the second item’s accordion body.</strong> It is hidden by default, until the collapse plugin adds the appropriate classes that we use to style each element. These classes control the overall appearance, as well as the showing and hiding via CSS transitions. You can modify any of this with custom CSS or overriding our default variables. It’s also worth noting that just about any HTML can go within the <code>.accordion-body</code>, though the transition does limit overflow.
                </div>
              </div>
            </div>
            <div class="accordion-item">
              <h2 class="accordion-header">
                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
                  Accordion Item #3
                </button>
              </h2>
              <div id="collapseThree" class="accordion-collapse collapse" data-bs-parent="#accordionExample">
                <div class="accordion-body">

                    <div class="card" style="width: 18rem;">
                      <img src="https://img-s-msn-com.akamaized.net/tenant/amp/entityid/AA1SKKR2.img?w=268&h=140&q=60&m=6&f=jpg&x=821&y=224&u=t" class="card-img-top" alt="first iamge miss">
                      <div class="card-body">
                        <h5 class="card-title">三角戀太精彩!孫淑媚《舊金山美容院》告白連晨翔 劉品言怒轟渣男</h5>
                        <p class="card-text">TVBS原創戲劇《舊金山美容院》中美食競賽的劇情發展進入高潮，觀眾見證了連晨翔因對手操控比賽而被淘汰的戲劇性時刻。劇中章廣辰意外聽到廁所內關於比賽操控的對話，隨後發現對手暗中操作，進而借題發揮、暗中操作比賽結果。劇情高潮不僅在比賽黑幕揭露，更延伸至感情世界，當連晨翔與製作人孫淑媚因「碰到親10秒送肉活動」而被劉品言撞見，引發三人情感衝突，最終在孫淑媚的脫口秀中全面爆發。</p>
                        <a href="https://reurl.cc/rKkEyy" class="btn btn-primary">connect</a>
                      </div>
                    </div>
                
                
                
                
                </div>
              </div>
            </div>
          </div>  
               
        </div>

        
        <div class="col-sm-4">
        <h1>BMI</h1>
            <div class="card shadow p-4">
              <h2 class="text-center mb-4">BMI 計算器</h2>
      
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



      
      <div class="row">
        <div class="col-2 p-3 mb-2 bg-primary text-white ">col</div>
        <div class="col-8 p-3 mb-2 bg-secondary text-white">col</div>
        <div class="col-2 p-3 mb-2 bg-success text-white">col</div>
      </div>
    


      <div class="row justify-content-center">
          <div class="col-12 col-md-6 col-lg-3 p-3 mb-2 bg-primary text-white">

          <div class="card" style="width: 18rem;">
            <img src="https://img-s-msn-com.akamaized.net/tenant/amp/entityid/AA1SKKR2.img?w=268&h=140&q=60&m=6&f=jpg&x=821&y=224&u=t" class="card-img-top" alt="first iamge miss">
            <div class="card-body">
              <h5 class="card-title">三角戀太精彩!孫淑媚《舊金山美容院》告白連晨翔 劉品言怒轟渣男</h5>
              <p class="card-text">TVBS原創戲劇《舊金山美容院》中美食競賽的劇情發展進入高潮，觀眾見證了連晨翔因對手操控比賽而被淘汰的戲劇性時刻。劇中章廣辰意外聽到廁所內關於比賽操控的對話，隨後發現對手暗中操作，進而借題發揮、暗中操作比賽結果。劇情高潮不僅在比賽黑幕揭露，更延伸至感情世界，當連晨翔與製作人孫淑媚因「碰到親10秒送肉活動」而被劉品言撞見，引發三人情感衝突，最終在孫淑媚的脫口秀中全面爆發。</p>
              <a href="https://reurl.cc/rKkEyy" class="btn btn-primary">connect</a>
            </div>
          </div>

            
          </div>
          <div class="col-12 col-md-6 col-lg-3 p-3 mb-2 bg-secondary text-white">

          <div class="card" style="width: 18rem;">
            <img src="https://img-s-msn-com.akamaized.net/tenant/amp/entityid/AA1SNnlR.img?w=268&h=140&q=60&m=6&f=jpg&u=t" class="card-img-top" alt="...">
            <div class="card-body">
              <h5 class="card-title">Card title</h5>
              <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card’s content.</p>
              <a href="#" class="btn btn-primary">Go somewhere</a>
            </div>
          </div>



            
          </div>
          <div class="col-12 col-md-6 col-lg-3 p-3 mb-2 bg-success text-white">


          <div class="card" style="width: 18rem;">
            <img src="..." class="card-img-top" alt="...">
            <div class="card-body">
              <h5 class="card-title">Card title</h5>
              <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card’s content.</p>
              <a href="#" class="btn btn-primary">Go somewhere</a>
            </div>
          </div>

            
          </div>
          <div class="col-12 col-md-6 col-lg-3 p-3 mb-2 bg-warning text-white">

          <div class="card" style="width: 18rem;">
            <img src="..." class="card-img-top" alt="...">
            <div class="card-body">
              <h5 class="card-title">Card title</h5>
              <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card’s content.</p>
              <a href="#" class="btn btn-primary">Go somewhere</a>
            </div>
          </div>

            
          </div>
      </div>
  </div>  
  </body>
</html>
