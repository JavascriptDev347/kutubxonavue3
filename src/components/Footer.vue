<template>
  <footer class="bg-dark text-center text-white">
    <div class="container p-4">
      <div class="container p-4 pb-0">
        <section class="mb-4">
          <section class="mb-4">
            <p>
              {{ $t("contact") }}
            </p>
          </section>
          <!-- Facebook -->
          <a
            class="btn btn-primary btn-floating m-1"
            style="background-color: #3b5998"
            href="https://www.facebook.com/hasan.sirojiddinov.1"
            role="button"
            ><i class="fab fa-facebook-f"></i
          ></a>

          <!-- Google -->
          <a
            class="btn btn-primary btn-floating m-1"
            style="background-color: #dd4b39"
            href="mailto:sirojiddinovkhasan@gmail.com"
            role="button"
            ><i class="fab fa-google"></i
          ></a>

          <!-- Instagram -->
          <a
            class="btn btn-primary btn-floating m-1"
            style="background-color: #ac2bac"
            href="https://www.instagram.com/accounts/login/?next=/i_khasan/"
            role="button"
            ><i class="fab fa-instagram"></i
          ></a>

          <!-- Telegram -->
          <a
            class="btn btn-primary btn-floating m-1"
            style="background-color: #0082ca"
            href="https://telegram.me/I_Khasan"
            role="button"
            ><i class="fab fa-telegram"></i
          ></a>
        </section>
      </div>

      <section class="">
        <div class="row">
          <div class="col-lg-6 col-md-6 mb-4 mb-md-0">
            <h5 class="text-uppercase">
              <span>{{ $t("useful_links") }}</span>
            </h5>

            <ul class="list-unstyled mb-0">
              <li>
                <router-link to="/" class="router text-white">{{
                  $t("home")
                }}</router-link>
              </li>
              <li>
                <router-link to="/books" class="router text-white">{{
                  $t("books")
                }}</router-link>
              </li>
              <li>
                <router-link to="/news" class="router text-white">
                  {{ $t("news") }}</router-link
                >
              </li>
              <li>
                <router-link to="/about_library" class="router text-white">
                  {{ $t("about_library") }}</router-link
                >
              </li>
            </ul>
          </div>

          <div class="col-lg-6 col-md-6 mb-4 mb-md-0">
            <h5 class="text-uppercase">{{ $t("library_links") }}</h5>

            <ul class="list-unstyled mb-0">
              <li>
                <a href="https://libraries.mit.edu/" class="text-white">{{
                  $t("MIT_Library")
                }}</a>
              </li>
              <li>
                <a href="https://library.harvard.edu/" class="text-white">{{
                  $t("Harvard")
                }}</a>
              </li>
              <li>
                <a href="https://www.natlib.uz/" class="text-white">{{
                  $t("Uzb")
                }}</a>
              </li>
            </ul>
          </div>
        </div>
      </section>
    </div>

    <div class="text-center p-3" style="background-color: rgba(0, 0, 0, 0.2)">
      © 2022 TATU
    </div>
  </footer>
</template>
