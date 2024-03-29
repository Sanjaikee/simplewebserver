# EX01 Developing a Simple Webserver
## Date:
29/03/2024
## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Home - Saveetha (Autonomous) Engineering College</title>
    <link rel="icon" href="saveetha.png">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css">
    <link rel="stylesheet" href="bootstrap.min.css">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" 
    rel="stylesheet" 
    integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" 
    crossorigin="anonymous">
    <style>
               .row1
        {
            background-color:#d5d3cb;display:flex;height: 62px;padding-inline: 10px;align-items: center; padding-bottom: 7px;
        }
        
        a
        {
            color: #cc324b;padding: 10px;text-decoration: none; font-family:  Arial; font-size: 15px; text-align: center; font-size: 15px;
        }
        a:hover
        {
            color:#52524a;
        }
        
        .row2
        {            
             background-color:white;display: flex;height:120px;
        }
       .row3
       {
           height:600px; background-color:#eeeeee; display:flex;text-decoration:none ;
       }
       .row4
       {
          height: 14px; background-color: gainsboro;
       }
       .row5
       {
        height: 186px; background-color: #eeeeee; display: flex;
       }
       .row6
       {
        height: 20px; background-color: #eeeeee;
       }
       .row7
      {
        height: 650px; background-color:#eeeeee; display: flex;font-family: Arial;height: 650px;
        
      }
      .row8
      {
        height: 100px;background-color: #eeeeee;
      }
      .row9
      {
        height:900px;background-color:#eeeeee;
      }
      

    </style>
</head>
<body>
    <div class="row1">
       
            <div style="width: 4%; background-color: #d5d3cb; height: 40px;color: red;">By, SANJAI</div>
            <div style="width: 30%; background-color: #d5d3cb; height: 40px;align-items:baseline; padding: 10px;">
                <a href="https://twitter.com/SaveethaSEC"><i class="bi bi-twitter" ></i></a>
                <a href="https://www.facebook.com/SaveethaEngineeringCollegeSEC/"><i class="bi bi-facebook"  ></i></a>
                <a href="https://studio.youtube.com/channel/UC8IBfXWNGSQkyUl95U4RU6A/videos"><i class="bi bi-youtube" ></i></a>
                <a href="https://www.linkedin.com/in/saveetha-engineering-college/"><i class="bi bi-linkedin" ></i></a>
                <a href="https://in.pinterest.com/saveethaengineeringcollege/"><i class="bi bi-pinterest" ></i></a>
                <a href="https://api.whatsapp.com/send?phone=+918939902737"><i class="bi bi-whatsapp" ></i></a>
                <a href="https://www.instagram.com/saveethaengineeringcollege/"><i class="bi bi-instagram" ></i></a>
            </div>
            <div style="width: 45%; background-color: #d5d3cb;height: 40px;padding: 10px; text-align: right ;">
                <a href="" >Alumini<i class="bi bi-three-dots-vertical"></i></a>
                <a href="" >Events<i class="bi bi-three-dots-vertical"></i></a>
                <a href="" >Career<i class="bi bi-three-dots-vertical"></i></a>
                <a href="" >Login<i class="bi bi-three-dots-vertical"></i></a>
                <a href="" >SEC Portal</i></a>
            </div> 
            <div style="width: 15%; background-color:transparent;height:40px;padding: 1px;">
                <div style="border: 1px solid; border-radius: 20px; padding-left: 1%;align-items: normal;">
                    <i class="bi bi-search"></i>
                <input type="text" placeholder="search..." style="height: 40px;background-color:#d5d3cb;border:0px; outline: none;padding: 1%; size-adjust: 10px;">
                </div>
            </div>
     </div>
    <div class="row2" style="border: 3%; position:-webkit-sticky;">
        <div style="width: 6%; background-color: #d5d3cb;color: red;font-size: 12px;">(212223230186)</div>
        <div class="col-3" style="background-color: white; border: 1px;"><img src="Saveethalogo.png" alt="saveetha" style="width: 100%; padding-top: 8%;"></div>
        <div class="col-6" style="background-color: white; font-size: 50px;padding-left: 2%; color: #cc324b;">
            <a href="">Home</a>
            <a href="">About</a>
            <a href="">Departments</a>
            <a href="">Life at SEC</a>
            <a href="">Admissions</a>
            <a href="">Placements</a>
            <a href="">Research</a>
        </div>
        <div class="col-1" style="background-color:#b1b1a9;width: 12%;height: 100px; position: relative;top: 10px;width: 12%;">
        <div style="color: #eeeeee; font-size: 20px; text-align: center;padding: 1%;">FOR </div>
        <div style="color: #eeeeee; font-size: 20px; text-align: center;padding: 1%;">ADMISSION</div>
        <div style="color: #eeeeee; font-size: 20px; text-align: center;padding: 1px;"><i class="bi bi-whatsapp"  ></i><a href="https://api.whatsapp.com/send?phone=+918939902737" style="color: cc324b;">8939902737</a></div>
        </div>
        <div class="col-1" style="background-color: #d5d3cb; width: 7%;"></div>
    </div>
    <div style="height: 15px; background-color: #eeeeee;"></div>

    <div class="row3">
        <div class="col-1" style="width: 6%;background-color: transparent; "></div>
         <div class="col-2" style="background-color:#cc324b; text-align:left;padding: 10px;font-size: 30px; border-radius: 10px;">
            <p><div style=" padding-left: 8%;padding-top: 3%;color: white;font-size: 20pt; align-items: center;">ADMISSION ENQUIRY<button type="button" class="btn btn-light">APPLY NOW</button></div></p>
          
          <div style="background-color: rgba(204, 50, 75, 0.3);height: 15px;border-bottom: dashed;color: rgb(230, 221, 221);;"></div>
            <div style="background-color: rgba(204, 50, 75, 0.3);;height: 15px;"></div>
          <p><div style=" padding-left: 8%;padding-top: 3%;color: white;font-size: 20pt; align-items: center;">Chat with Student Ambassador <button type="button" class="btn btn-light">KNOW MORE</button></div></p>
          
          <div style="background-color: rgba(204, 50, 75, 0.3);height: 15px;border-bottom: dashed;color: rgb(230, 221, 221);;"></div>
            <div style="background-color: rgba(204, 50, 75, 0.3);;height: 15px;"></div>
          <p><div style=" padding-left: 8%;padding-top: 3%;color: white;font-size: 20pt; align-items: center;">BLOGS </div><button type="button" class="btn btn-light" style="padding-right: 27px;padding-left: 10px;">KNOW MORE</button></p>
          </div>
          <div style="background-color:transparent; width: 18px;"></div>
          <div class="col-8" style="background-color: transparent; width: 69%;padding-left: 2px; border-radius: 10px;">
            <div id="carouselExampleIndicators" class="carousel slide" style="height: 600px;">
                <div class="carousel-indicators"  style="height: 300px;">
                  <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
                  <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="1" aria-label="Slide 2"></button>
                  <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="2" aria-label="Slide 3"></button>
                </div>
                <div class="carousel-inner" style="height: 600px;">
                  <div class="carousel-item active">
                    <img src="imgggg.png" class="d-block w-100" alt="saveetha">
                  </div>
                  <div class="carousel-item">
                    <img src="kkkkk.png" class="d-block w-100" alt="saveetha">
                  </div>
                  <div class="carousel-item">
                    <img src="Screenshot 2024-03-27 221829.png" class="d-block w-100" alt="saveetha">
                  </div>
                  <div class="carousel-item">
                    <img src="Screenshot 2024-03-27 221753.png" class="d-block w-100" alt="saveetha">
                  </div>
                  <div class="carousel-item">
                    <img src="Screenshot 2024-03-27 221721.png" class="d-block w-100" alt="saveetha">
                  </div>
                </div>
                <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="prev">
                  <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                  <span class="visually-hidden">Previous</span>
                </button>
                <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="next">
                  <span class="carousel-control-next-icon" aria-hidden="true"></span>
                  <span class="visually-hidden">Next</span>
                </button>
              </div>
          </div>
          
        </div>
        
    </div>
   
    <div class="row4" style="background-color:#eeeeee;"></div>
    <div class="row5" >
         <div class="col-1" style="background-color:transparent;width: 6%; height: 186px; "></div>
         
            <div style="display: flex;height: 180px;position:relative;top: 14px; height: 170px; position: relative;right: 50px;;">
                <img src="fg.jpg" style="width:19%;padding: 15px; position: relative; left: 60px;">
                <img src="gh.jpg" style="width:19%;padding: 15px;position: relative;left: 110px;">
                <img src="df.jpg" style="width:19%;padding: 15px;position: relative;left: 150px ;">
                <img src="sd.jpg" style="width:19%;padding: 15px;position: relative; left: 200px;">
                <img src="as.jpg" style="width:19%;padding: 15px;position: relative;left: 230px;">
            </div>
    </div>
    <div class="col-1" style="background-color:black;width: 6%;;"></div>
    <div class="row6" >
                
     </div>
    

    <div class="row7" style="display: flex;font-weight: 100px;">
          <div class="col-1" style="width: 6%;background-color:#eeeeee;"></div>
          <div class="col-2" style="background-color:#f3f3f3;">
              <div ><i class="bi bi-people" style="font-size: 300%; position: relative;top:40px;left: 10px;bottom: 30px;"></i><h2 style="text-align: right;position: relative;bottom: 40px;">32</h2>
                <h3 style="text-align: right; position: relative;bottom: 40px;">Centers of Excellence</h3></div>
                <hr style="position: relative;bottom: 40px;"></hr>
              <div ><i class="bi bi-people" style="font-size: 300%; position: relative;bottom:30px;left: 10px;"></i><h2 style="text-align: right;position: relative;bottom:120px;">256</h2>
                <h3 style="text-align: right;position: relative;bottom:120px;">MOUs with <div>Reputed</div> <div><h3>Industries</h3></div></h3></div>
                <hr style="position: relative;bottom: 120px;"></hr>
                <div ><i class="bi bi-people" style="font-size: 300%; position: relative;bottom:110px;left: 10px;"></i><h2 style="text-align: right;position: relative;bottom:200px;">3104</h2>
                  <h3 style="text-align: right;position: relative;bottom:200px;">Publications</h3></div>
                  <hr style="position: relative; bottom: 210px;"></hr>
                  <div style="height: 17px;background-color:transparent;position: relative;bottom: 220px; "></div>
                  <div ><iframe width="327" height="164" src="https://www.youtube.com/embed/mJltgvO4kL0" title="Embark on a future-engineering journey at Saveetha Engineering College (Chennai)" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen  style="width: 253px;position: relative;bottom: 220px;"></iframe></div>
                  <div style="width: max-width: ;; background-color:#eeeeee;position:relative; bottom:226px;height:54px;"></div>
                  
           </div>
           <div style="width: 17px;background-color:#eeeeee;height: 670px;"></div>
           <div class="col-6" style="height: 600px;">
            <div  style="height:670px;background-color: #f3f3f3;">
              <div><img src="tg.jpg" alt="saveetha" style="width: 100%; padding-top: 30px;padding-left: 25px;padding-right: 25px;"><div style="padding-left: 25px;padding-right: 25px;padding-top: 30px;">SEC is a leading Engineering College located in Chennai, India., which offers a global approach to education and research, with a focus on global perspectives and expertise. SEC offers a wide range of undergraduate, postgraduate and doctoral programs in Engineering. Some of its Academic Highlights are,</div>
              
            </div>
              <div style="padding-left: 40px;padding-top: 20px;">
                <div> 1. Only Engineering College in India to have 30 students per class.</div>
              <div> 2. 91% results in University exam.</div>
              <div> 3. 173 University Ranks.</div>
              <div> 4. Compulsory internship every year.</div></div>
            </div>
           </div>
          <div style="width: 17px;background-color:#eeeeee;height: 670px ;"></div>
          <div class="col-3" style="background-color: #f3f3f3; width: 270px;font-size: 24px;font-weight: 600;font-family: jura; color: #676767;padding-top: 30px;padding-left: 20px;">
             Latest event:
             <div style="font-weight:1; color: #52524a; font-size: 19px;position: relative;left: 20px;top: 23px;">06 Mar 2024;</div>
             <div style="color: #cc324b;font-weight: 700;text-decoration: none; cursor: pointer;text-align: left;position: relative;right: 5px;top: 15px; text-transform: none;text-indent: initial;"><a href=""><strong>AI&DS learners secured the Runner-Up position and won 'ARM Development Studio' worth ₹ 3.5 Crores</strong></a></div>
              <hr style="position: relative;top: 10px;right: 10px;">
              <div style="font-weight:1; color: #52524a; font-size: 19px;position: relative;left: 20px;top: 15px;">07 Mar 2024;</div>
              <div style="color: #cc324b;font-weight: 700;text-decoration: none; cursor: pointer;text-align: left;position: relative;right: 5px;top: 15px; text-transform: none;text-indent: initial;"><a href=""><strong>SEC offers 100% Merit Scholarships with a Fee Waiver</strong></a></div>
              <hr style="position: relative;top: 10px;right: 10px;">
              <div style="font-weight:1; color: #52524a; font-size: 19px;position: relative;left: 20px;top: 15px;">08 Mar 2024;</div>
              <div style="color: #cc324b;font-weight: 700;text-decoration: none; cursor: pointer;text-align: left;position: relative;right: 5px;top: 15px; text-transform: none;text-indent: initial;"><a href=""><strong>Ms. Rajalakshmi Srinivasan, Dir. of Product Management at Zoho visited the SEC campus</strong></a></div>
              <div style="background-color:#eeeeee;width: 44%;position: relative;left: 250px;top: 30px;color: #eeeeee;">.</div>

          </div>
          <div style="width: 6%; background-color: #eeeeee;"></div>

    </div>
    <div style="width: 6%;background-color: #eeeeee;height: 20px;position: relative;top: 1px;"></div>

    <div style="background-color: #eeeeee;height: 18px;"></div>


    <div class="row8" style="height: 360px; background-color:#eeeeee;display: flex;">
      <div class="col-1" style="background-color: transparent;width: 6%;"></div>
      
      
      <div class="col-3" style="background-color: #f3f3f3;width: 28%;">
        <div style="width: 85%;position: relative;left: 33px;padding-top: 33px;bottom:px;height: 50px;">
          <div id="carouselExampleSlidesOnly" class="carousel slide" data-bs-ride="carousel">
            <div class="carousel-inner" style="height: 300px;position: relative;bottom: 3px;">
              <div class="carousel-item active">
                <img src="qaz.jpg" class="d-block w-100" alt="...">
              </div>
              <div class="carousel-item">
                <img src="wsx.jpg" class="d-block w-100" alt="...">
              </div>
              <div class="carousel-item">
                <img src="edc.jpg" class="d-block w-100" alt="...">
              </div>
              <div class="carousel-item">
                <img src="rfv.jpg" class="d-block w-100" alt="...">
              </div>
            </div>
          </div>
        </div>

      
      
      
      </div>
      
      
      
      <div style="width: 20px; background-color: transparent;"></div>
      
      
      
      <div class="col-3" style="background-color: #f3f3f3;width: 28%;">
        <div style="width: 85%;position: relative;left: 33px;padding-top: 33px;bottom:px;height: 50px;">
          <div id="carouselExampleSlidesOnly" class="carousel slide" data-bs-ride="carousel">
            <div class="carousel-inner" style="height: 300px;position: relative;bottom: 3px;">
              <div class="carousel-item active">
                <img src="rf.jpg" class="d-block w-100" alt="...">
              </div>
              <div class="carousel-item">
                <img src="fv.jpg" class="d-block w-100" alt="...">
              </div>
              <div class="carousel-item">
                <img src="gb.jpg" class="d-block w-100" alt="...">
              </div>
              <div class="carousel-item">
                <img src="yh.jpg" class="d-block w-100" alt="...">
              </div>
            </div>
          </div>
        </div>
      
      
      
      
      </div>
      
      
      
      
      <div style="width: 20px; background-color:transparent;"></div>
      
      
      
      
      
      <div class="col-3" style="background-color: #f3f3f3;width: 28%;">
            <div style="width: 85%;position: relative;left: 33px;padding-top: 33px;bottom:px;height: 50px;">
              <div id="carouselExampleSlidesOnly" class="carousel slide" data-bs-ride="carousel">
                <div class="carousel-inner" style="height: 300px;position: relative;bottom: 3px;">
                  <div class="carousel-item active">
                    <img src="qa.jpg" class="d-block w-100" alt="...">
                  </div>
                  <div class="carousel-item">
                    <img src="az.jpg" class="d-block w-100" alt="...">
                  </div>
                  <div class="carousel-item">
                    <img src="ws.jpg" class="d-block w-100" alt="...">
                  </div>
                  <div class="carousel-item">
                    <img src="sx.jpg" class="d-block w-100" alt="...">
                  </div>
                </div>
              </div>
            </div>
      
      
      </div>
    
    
    </div>
    <div style="height: 20px;background-color: #eeeeee;"></div>
    

    <div class="row9" style="display: flex;">
          <div class="col-1" style="background-color: transparent;width: 6%;"></div>
          <div class="col-5" style="background-color: #f3f3f3;width: 43%;">
                    <div style="color: #52524a;font-weight: 1;font-family: 'Jura';font-size: 30px;position: relative;top: 15px; left:16px ;"><strong>Placements</strong></div>
                    <div><img src="okm.png" alt="Placements" style="width: 95%;position: relative;left: 16px;top: 35px;" ></div>
                    <div  style="font-size: 15px;font: inherit;position: relative;top: 80px;left: 16px;text-align: left;"><p>Saveetha Engineering College (SEC) has always been a favourite destination of recruitment for over 230+ Multinational companies and firms. Our focus on placement centers on creating new approaches to attract the best from the industry to our campus.</p></div>
                    <div style="position: relative;top: 150px;left: 30px;">
                      <div>1. 97% Placement in 2022 Batch.</div>
                      <div>2. 233 plus Multinational Company visited our Campus</div>
                      <div>3. 1302 Placement Offers</div>
                      <div>4. Highest CTC of Rs. 34 Lakhs per annum</div>
                      <div>5. Average CTC of Rs. 6.15 Lakhs per annum</div>


                    </div>
                     

                    
          
          </div>
          <div style="width: 20px;background-color: transparent;"></div>

          <div class="col-5" style="background-color:#f3f3f3;width: 43%;">
            <div style="color: #52524a;font-weight: 1;font-family: 'Jura';font-size: 30px;position: relative;top: 15px; left:16px ;margin: 5;box-shadow: #676767;"><strong>Testimonial</strong></div>
            <div style="width: 95%;position: relative;left: 16px;top: 35px;">
              <div id="carouselExampleSlidesOnly" class="carousel slide" data-bs-ride="carousel">
                <div class="carousel-inner">
                  <div class="carousel-item active">
                    <img src="1qa.jpg" class="d-block w-100" alt="...">
                  </div>
                  <div class="carousel-item">
                    <img src="2qa.jpg" class="d-block w-100" alt="...">
                  </div>
                  <div class="carousel-item">
                    <img src="3qa.jpg" class="d-block w-100" alt="...">
                  </div>
                  <div class="carousel-item">
                    <img src="4qa.jpg" class="d-block w-100" alt="...">
                  </div>
                  <div class="carousel-item">
                    <img src="5qa.jpg" class="d-block w-100" alt="...">
                  </div>
                  <div class="carousel-item">
                    <img src="6qa.jpg" class="d-block w-100" alt="...">
                  </div>
                  <div class="carousel-item">
                    <img src="7qa.jpg" class="d-block w-100" alt="...">
                  </div>
                  <div class="carousel-item">
                    <img src="8qa.jpg" class="d-block w-100" alt="...">
                  </div>
                  <div class="carousel-item">
                    <img src="9qa.jpg" class="d-block w-100" alt="...">
                  </div>
                </div>
              </div>

            </div>
          
          </div>
    </div>
  




    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" 
    integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" 
    crossorigin="anonymous"></script>
</body>
</html>

## OUTPUT:
![alt text](<Screenshot 2024-03-29 223534.png>)

## RESULT:
The program for implementing simple webserver is executed successfully.
