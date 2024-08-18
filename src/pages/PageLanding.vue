<template>
  <div>
    <section class="banner">
      <h2>Olá, meu nome é <br /><span>Pedro Oliveira</span></h2>
      <h3>E sou um desenvolvedor Fullstack.</h3>
      <a href="#about"
        ><q-btn class="btn" color="primary" label="Sobre Mim"
      /></a>
    </section>
    <section id="about" class="about">
      <div class="heading">
        <h2>Sobre Mim</h2>
      </div>
      <div class="content">
        <div class="contentBx w50">
          <h3>Sou um desenvolvedor Fullstack.</h3>
          <p>
            Iniciei minha carreira como programador em 2017. De lá pra cá, venho me aperfeiçoando cada vez mais, sempre
            em busca de novos desafios.
          </p>
          <br />
          <br />
          <p>
            Mas o que é um desenvolvedor Fullstack afinal?
          </p>
          <p>
            Bom, como Fullstack estou apto para atuar em todas as etapas do
            desenvolvimento de um sistema. Além de contribuir com o frontend e
            backend de uma aplicação, posso também delinear e concretizar a
            organização da infraestrutura, do banco de dados, e do
            desenvolvimento mobile.
          </p>
        </div>
        <div class="w50">
          <img src="../assets/images/img2.jpg" class="img" />
        </div>
      </div>
    </section>
    <section id="contact" class="contact">
      <div class="heading text-white">
        <h2>Entre em contato</h2>
        <p>O networking é o melhor caminho para um conhecimento mutuo.</p>
      </div>

      <div class="content text-white">
        <div class="contactInfo">
          <h3>Informações para contato</h3>
          <div class="contactInfoBx">
            <div class="box">
              <div class="icon">
                <q-icon name="fas fa-map-marker-alt"></q-icon>
              </div>
              <div class="text">
                <h3>Endereço</h3>
                <p>Brasília, Brasil</p>
              </div>
            </div>
            <div class="box">
              <div class="icon">
                <q-icon name="fas fa-phone"></q-icon>
              </div>
              <div class="text">
                <h3>Telefone</h3>
                <p>55 61 998190889</p>
              </div>
            </div>
            <div class="box">
              <div class="icon">
                <q-icon name="fas fa-envelope"></q-icon>
              </div>
              <div class="text">
                <h3>Email</h3>
                <p>pedro.dev.oliveira@gmail.com</p>
              </div>
            </div>
          </div>
        </div>

        <div class="formBx">
          <q-form>
            <h3>Mande uma mensagem</h3>
            <q-input
              dark
              filled
              type="text"
              bg-color="grey-10"
              label-color="white"
              label="Nome completo"
              class="input"
              v-model="lead.name"
            />
            <q-input
              dark
              filled
              type="email"
              bg-color="grey-10"
              label-color="white"
              label="Email"
              class="input"
              v-model="lead.email"
            />
            <q-input
              dark
              filled
              type="textarea"
              bg-color="grey-10"
              label-color="white"
              label="Sua mensagem"
              class="input"
              v-model="lead.message"
            />

            <div>
              <q-btn label="Enviar" type="submit" color="primary" />
            </div>
          </q-form>
          <div class="social-media">
            <a
              href="https://www.linkedin.com/in/pedro-oliveira-dev/"
              target="_blank"
            >
              <q-icon name="fab fa-linkedin-in" />
            </a>
            <a href="https://github.com/PedroUnb" target="_blank">
              <q-icon name="fab fa-github" />
            </a>
            <a
              href="https://api.whatsapp.com/send?phone=5561998190889&text=Olá Pedro, encontrei o seu número atravéz do seu site."
              target="_blank"
            >
              <q-icon name="fab fa-whatsapp" />
            </a>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      lead: {
        name: "",
        email: "",
        message: ""
      }
    };
  }
};
</script>

<style lang="scss">
section {
  padding: 100px;
}

.banner {
  position: relative;
  min-height: 100vh;
  background: url("../assets/images/banner.jpg");
  background-size: cover;
  background-position: right;
  display: flex;
  justify-content: center;
  align-items: flex-start;
  flex-direction: column;
  align-content: center;
  flex-wrap: nowrap;

  h2 {
    font-size: 3em;
    color: #fff;
    font-weight: 500;
    line-height: 1.5em;
  }

  h2 span {
    font-size: 1.5em;
    font-weight: 700;
  }

  h3 {
    font-size: 1.5em;
    color: #fff;
    font-weight: 500;
  }

  a {
    text-decoration: none;
  }

  .btn {
    margin-top: 20px;
    letter-spacing: 2px;
    font-weight: 500;
    font-size: 18px;
  }
}

.heading {
  width: 100%;
  text-align: center;
  margin-bottom: 30px;
  color: #111;
}

.heading h2 {
  font-weight: 600;
  font-size: 30px;
}

.about {
  .content {
    display: flex;
    justify-content: space-between;

    .contentBx {
      padding-right: 30px;
    }

    .contentBx h3 {
      font-size: 24px;
      margin-bottom: 10px;
    }

    .w50 {
      min-width: 50%;
    }

    img {
      max-width: 100%;
    }
  }
}

.contact {
  background: #111;

  .content {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    align-content: stretch;
    justify-content: space-around;
    align-items: flex-start;
  }

  .formBx {
    min-width: 60%;

    form {
      display: flex;
      flex-direction: column;

      .input {
        margin-bottom: 20px;
        font-size: 16px;
      }

      textarea {
        resize: none;
      }
    }

    .social-media {
      font-size: 26px;
      margin-top: 20px;
      text-align: -webkit-right;

      a {
        text-decoration: none;
        color: #fff;
        padding: 10px;
      }
    }
  }

  .contactInfo {
    min-width: 40%;
    .contactInfoBx {
      position: relative;

      .box {
        position: relative;
        padding: 20px 0;
        display: flex;

        .icon {
          min-width: 40px;
          padding-top: 14px;
          display: flex;
          justify-content: center;
          align-items: flex-start;
          font-size: 24px;
        }

        .text {
          display: flex;
          margin-left: 20px;
          font-size: 16px;
          flex-direction: column;
          font-weight: 300;

          h3 {
            font-weight: 500;
            color: $primary;
            margin-bottom: 0px;
          }
        }
      }
    }
  }

  .formBx form,
  .contactInfo {
    h3 {
      font-size: 20px;
      font-weight: 500;
      margin-bottom: 1px;
    }
  }
}

@media (max-width: 991px) {
  section {
    padding: 100px 50px;
  }

  .banner {
    padding: 150px 50px 100px;
  }

  .banner h2 {
    font-size: 1.5em;
  }

  .banner h3 {
    font-size: 1em;
  }

  .banner .btn {
    margin-top: 5px;
    padding: 5px 10px;
    font-size: 12px;
  }

  .content {
    flex-direction: column;
  }
}
</style>
