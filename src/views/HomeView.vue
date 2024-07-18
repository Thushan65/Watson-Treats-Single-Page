<script setup>
import Thefotter from '../components/footer.vue'
</script>

<template>
  <main id="home">
    <h1>Watson Treats</h1>
    <p id="moto">"Indulge in sweetness at Watson Treats, where every visit promises a slice of joy and a taste of perfection. Join us for an exquisite cake experience in the heart of Liverpool!"</p>
    <img src="/images/f1.jpg" alt="Picture of a cake shop" width="100%" height="250px">
    <br>

    <div id="about">
    <h2>About Us</h2>
    <p>Welcome to Watson Treats, where every visit promises a delectable journey through the world of exquisite desserts and indulgent delights. Nestled in the heart of Liverpool, our charming cake shop invites you to experience the artistry and passion infused into every sweet creation. From our signature cakes adorned with intricate designs to our tempting array of pastries and confections, each treat is crafted with care and creativity to tantalize your taste buds. Step into our cozy haven and let the aroma of freshly baked goods envelop you as you explore our delectable offerings. Whether you're stopping by for a quick pick-me-up or planning a special event, Watson Treats is your ultimate destination for all things sweet and delightful. Come, indulge your senses and embark on a culinary adventure with us.</p>
    </div>


    <div id="links">
      <div>
        <a href="/cakes">
        <h2>Our Cakes</h2>
        <img src="/images/Cake_Home.jpg" alt="Our cakes" width="400px" height="400px">
      </a>
      </div>
      <div>
        <a href="/events">
        <h2>Plan Your Events With Us</h2>
        <img src="/images/catering2.jpg" alt="Our Events" width="400px" height="400px">
      </a>
      </div>
    </div>

    <div id="visit">
      <h2>Visit US</h2>
      <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d76111.16112675396!2d-3.0143892248660875!3d53.406352420853075!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x487adf8a647060b7%3A0x42dc046f3f176e01!2sLiverpool!5e0!3m2!1sen!2suk!4v1715363544015!5m2!1sen!2suk" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    </div>

    <div id="customer">
      <h2>What Our Customers Say?</h2>
      <p>Hear some stories from our valueable customers about their incredible experience with us.</p>
      <br><br>
    </div>
        <div id="feedback">
            <div>
              <img src="/images/Feedback1.jpg" alt="Feedback1" width="200px" height="200px">
              <p>"Watson Treats in Liverpool crafts cakes that are pure artistry. From their stunning designs to the exquisite flavors, every bite is a celebration of taste and creativity!"</p>
              <h4>(4.6)</h4>
              <h3>Maria Smith</h3>
            </div>
            <div>
              <img src="/images/Feedback2.jpg" alt="Feedback2" width="200px" height="200px">
              <p>"At Watson Treats in Liverpool, the cakes are exceptional! With a diverse range of flavors and top-notch quality, it's a sweet haven for anyone seeking delicious treats in the city."</p>
              <h4>(4.5)</h4>
              <h3>Jack Lloyds</h3>
            </div>
        </div>
    <Thefotter/>
  </main>
</template>


<style lang="scss" scoped>

$font-main: Merriweather, Helvetica, sans-serif;

$font-highlight: Bree Serif, Helvetica, sans-serif;

$offwhite: #EEE8D6;

$darkblue: #022933;

$orange: #F39856;

$red: #D14348;

$purple: #6D73C2;

$colour-text: $darkblue;

$colour-backgrounds: $offwhite;

$colour-headlines: $red;

#home {

font-family:$font-highlight;

background-color:$colour-backgrounds;

color:$colour-text;

  h1 {
  text-align: center;
  color:$colour-text;
  font-size: 400%;
  }
}

#moto{
  text-align: center;
}

#about{
  border-style: solid;
  border-color: #022933;
  margin: 1% 1% 1% 1%;
  h2{
    margin-left: 2%;
  }
  p{
    margin: 5px 5px 5px 5px;
    text-align: center;
  }
}

#links{
  display:grid;
  grid-template-columns:repeat(2,minmax(100px, 2fr));
  margin-left: 1%;
  margin-right: 1%;
  h2{
    text-align: center;
    color: #022933;
    border-bottom-style: solid;
    border-bottom-color: #022933;
  }

  img{
    border-radius: 5px;
    margin-left: 190px;
  }

  div{
    border-style: solid;
    border-color: #022933;
  }
}

#visit{
  h2{
    text-align: center;
    font-size: xx-large;
  }
  iframe{
    border-radius: 5px;
    margin-left: 470px;
  }
}

#feedback{
  display:grid;
  grid-template-columns:repeat(2,minmax(100px, 2fr));
  text-align: center;
  p{
    margin-left: 1%;
    margin-right: 1%;
  }
}

#customer{
  h2,p{
    margin-left: 2%;
  }
}

</style>
