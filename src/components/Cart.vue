 <script>
 
 </script>


<template>
  <div class="container">
    <div class="shopping-cart">
      <div class="shopping-cart-header">
        <i class="fa fa-shopping-cart cart-icon"></i
        ><span class="badge">0</span>
        <div class="shopping-cart-total">
          <span class="lighter-text">Total:</span>
          <span class="main-color-text"></span>
        </div>
      </div>
      <!--end shopping-cart-header -->

      <ul class="shopping-cart-items">
        <li class="clearfix"></li>
      </ul>

      <a href="#" class="button">Buy</a>
    </div>
    <!--end shopping-cart -->
  </div>
  <!--end container -->
</template>
<style lang="scss" scoped>
$main-color: #6394f8;
$light-text: #abb0be;

@import url(https://fonts.googleapis.com/css?family=Lato:300,400,700);

@import url(https://maxcdn.bootstrapcdn.com/font-awesome/4.4.0/css/font-awesome.min.css);

*,
*:before,
*:after {
  box-sizing: border-box;
}

body {
  font: 14px/22px "Lato", Arial, sans-serif;
  background: #6394f8;
}

.lighter-text {
  color: #abb0be;
}

.main-color-text {
  color: $main-color;
}

nav {
  padding: 20px 0 40px 0;
  background: #f8f8f8;
  font-size: 16px;

  .navbar-left {
    float: left;
  }

  .navbar-right {
    float: right;
  }
  ul {
    li {
      display: inline;
      padding-left: 20px;
      a {
        color: #777777;
        text-decoration: none;

        &:hover {
          color: black;
        }
      }
    }
  }
}

.container {
  margin: auto;
  width: 80%;
}

.badge {
  background-color: #6394f8;
  border-radius: 10px;
  color: white;
  display: inline-block;
  font-size: 12px;
  line-height: 1;
  padding: 3px 7px;
  text-align: center;
  vertical-align: middle;
  white-space: nowrap;
}

.shopping-cart {
  background: white;
    width: 320px;
    position: absolute;
    border-radius: 3px;
    padding: 20px;
    right: 50px;
  
  
  .shopping-cart-header {
    border-bottom: 1px solid #e8e8e8;
    padding-bottom: 15px;

    .shopping-cart-total {
      float: right;
    }
  }

  .shopping-cart-items {
    padding-top: 20px;

    li {
      margin-bottom: 18px;
    }

    img {
      float: left;
      margin-right: 12px;
    }

    .item-name {
      display: block;
      padding-top: 10px;
      font-size: 16px;
    }

    .item-price {
      color: $main-color;
      margin-right: 8px;
    }

    .item-quantity {
      color: $light-text;
    }
  }
}

.shopping-cart:after {
  bottom: 100%;
  left: 89%;
  border: solid transparent;
  content: " ";
  height: 0;
  width: 0;
  position: absolute;
  pointer-events: none;
  border-bottom-color: white;
  border-width: 8px;
  margin-left: -8px;
}

.cart-icon {
  color: #515783;
  font-size: 24px;
  margin-right: 7px;
  float: left;
}

.button {
  background: $main-color;
  color: white;
  text-align: center;
  padding: 12px;
  text-decoration: none;
  display: block;
  border-radius: 3px;
  font-size: 16px;
  margin: 25px 0 15px 0;

  &:hover {
    background: lighten($main-color, 3%);
  }
}

.clearfix:after {
  content: "";
  display: table;
  clear: both;
}
</style>
