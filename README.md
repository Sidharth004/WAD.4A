# WAD.4A
Jquery mobile : minimalistic frontend


#WAD- ANGULAR

APP COMPNENT .TS

import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent {
  title = 'Registration form';

  displayname ="";
  displayemail="";
  displayaddress="";
  displaypassword="";

  getValue(name:string, email:string , address: string, password: string){
    this.displayname = name;
    this.displayemail = email;
    this.displayaddress = address;
    this.displaypassword = password; 
  }
}



APP COMPONENT.HTML
<h1>{{title}} </h1> 
<!-- data binding -->

<input type="text" placeholder="Name here" #name name="Name"><br>

<input type="email" placeholder="Email here" #email name="Email"> <br>

<input type="text" placeholder="Address here" #address name="Address"><br> 

<input type="password" placeholder="Password here" #password name="Password"><br> 

<!-- create a button to pass the form values through it -->
<button (click)="getValue(name.value, email.value, address.value, password.value)">Register</button>

<!-- displaying stored data -->

<h2>Here's the details</h2>

<p>Name : {{displayname}}</p>
<p>Email : {{displayemail}}</p>
<p>Address : {{displayaddress}}</p>
<p>Password : {{displaypassword}}</p>
###############################################################################################################################################
#################################################################################################################
BOOTSTRAP -HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-KK94CHFLLe+nY2dmCWGMq91rCGa5gtU4mk92HdvYe+M/SXH301p5ILy+dN9+nJOZ" crossorigin="anonymous">
    <link rel="stylesheet" href="styles.css">
    <title>Dashboard</title>
</head>
<body>
    
    <!-- navbar -->
    <nav class="navbar " style="background-color: aquamarine;">
        <div class="container-fluid">
          <a class="navbar-brand">Dashboard</a>
          <form class="d-flex" role="search">
            <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
            <button class="btn btn-outline-success" type="submit">Search</button>
            <!-- nav buttons -->
            <button type="button" class="btn btn-primary">Primary</button>
            <button type="button" class="btn btn-secondary">Secondary</button>
          </form>
          
        </div>
    </nav>

    <!-- sidebar -->
    <div class="container-fluid">
        <div class="row">
            <nav class="col-md-2 d-none d-md-block bg-light sidebar position-fixed">
                <div class="sidebar-sticky">
                    <ul class="nav flex-column nav-pills">   
                        <li class="nav-item">
                            <a class="navlin active"ahref="#">
                                <span>Dashboard</span>
                            </a>
                        </li>
                        <a class="nav-link active" aria-current="page" href="#">Active</a>
                        <a class="nav-link" href="#">Link</a>
                        <a class="nav-link" href="#">Link</a>
                        <a class="nav-link disabled">Disabled</a>

                    </ul>
                </div>
            </nav>
        </div>

    </div>

    <!-- content -->
    <div class="col-md-9  ms-sm-auto col-lg-10 px-md-4">
    <!-- content jere -->
    <!-- row wise -->
    <div class="row">
        <div class="col-md-12">
            <h1>Hi there</h1>
            <p>Content 1st card</p>
        </div>
        <!-- each card row : col-md-5  col-lg-6 -->
        <div class="col-md-5 col-lg-6">
            <!-- 30 rem width -->
        <div class="card" style="width: 30rem;">
            <img src="https://cdn.simplekpi.com/images/Resources/column-chart.webp" class="card-img-top" alt="...">
            <div class="card-body">
              <h5 class="card-title">Card title</h5>
              <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
            </div>
            <ul class="list-group list-group-flush">
              <li class="list-group-item">An item</li>
            </ul>
            <div class="card-body">
              <a href="#" class="card-link">Card link</a>
              <a href="#" class="card-link">Another link</a>
            </div>
          </div>
        </div>
        <!-- row 1 col 2nd -->
        <div class="col-md-5 col-lg-6">
          <div class="card" style="width: 30rem;">
            <img src="https://images.nagwa.com/figures/970171409850/1.svg" id='img2'class="card-img-top" alt="...">
            <div class="card-body">
              <h5 class="card-title">Card title</h5>
              <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
            </div>
            <ul class="list-group list-group-flush">
              <li class="list-group-item">An item</li>
             
            </ul>
            <div class="card-body">
              <a href="#" class="card-link">Card link</a>
              <a href="#" class="card-link">Another link</a>
            </div>

          </div>
        </div>
        
        
        <div class="row">
            <div class="col-lg-4 col-md-4">
                <div class="card " style="width: 20rem;">
                  <img src="" class="card-img-top" alt="...">
                  <div class="card-body">
                    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
                  </div>
                </div>
            </div>
            <div class="col-lg-4 col-md-4">
                <figure class="figure">
                    <img src="..." class="figure-img img-fluid rounded" alt="...">
                    <figcaption class="figure-caption">A caption for the above image.</figcaption>
                </figure>
            </div>
        </div>
        

        
    </div>
</div> 
    
</body>
</html>


######BOOTSTRAP CSS:
.sidebar{
    position: sticky;
    top: 0;
    height: 100vh;
}

.card{
    margin:1px;
    margin-bottom: 20px;
    
}

.card #img2{
    width: 258px;
    
}

button{
    margin: 2px;
}
