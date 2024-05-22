<template>
  <q-layout view="hHh lpR fFf">
    <q-header elevated class="bg-pink text-white" height-hint="98">
      <div class="q-pa-md q-gutter-sm">
        <q-bar class="bg-black text-white">
          <q-btn dense flat icon="fab fa-apple" />
          <div class="text-weight-bold">warung kevin</div>
          <div class="cursor-pointer gt-md text-blue">pesan</div>
          <div class="cursor-pointer gt-md text-pink">keranjang</div>
          <div class="cursor-pointer gt-md text-green">alamat</div>
          <q-space />
          <q-btn dense flat icon="airplay" class="gt-xs" />
          <q-btn dense flat icon="battery_charging_full" />
          <q-btn dense flat icon="wifi" />
          <div>9:41</div>
          <q-btn dense flat icon="search" />
          <q-btn dense flat icon="list" />
        </q-bar>

        <q-bar>
          <q-btn dense flat round icon="lens" size="8.5px" color="red" />
          <q-btn dense flat round icon="lens" size="8.5px" color="yellow" />
          <q-btn dense flat round icon="lens" size="8.5px" color="green" />
          <div class="col text-center text-weight-bold">KUE KEVIN</div>
        </q-bar>
      </div>
    </q-header>

    <q-drawer show-if-above v-model="leftDrawerOpen" side="left" bordered>
      <!-- drawer content -->
    </q-drawer>

    <q-drawer show-if-above v-model="rightDrawerOpen" side="right" bordered>
      <!-- drawer content -->
    </q-drawer>

    <q-page-container>
      <q-page class="q-pa-md">
        <q-carousel
          animated
          v-model="slide"
          arrows
          navigation
          infinite
        >
          <q-carousel-slide :name="1" img-src="https://image.makewebeasy.net/makeweb/m_1920x0/rGAbosWut/DefaultData/AGS_0543_min.jpg" />
          <q-carousel-slide :name="2" img-src="https://d1vbn70lmn1nqe.cloudfront.net/prod/wp-content/uploads/2023/07/24072104/Resep-Kue-Ulang-Tahun-Rumahan-Sederhana-dan-Elegan-.jpg.webp" />
          <q-carousel-slide :name="3" img-src="https://cdn.idntimes.com/content-images/community/2024/01/1705315841922-050d7c823376e5868043b1f6ae8078e6-ba3b77672d25449256c943e3656b16ed.jpg" />
          <q-carousel-slide :name="4" img-src="https://image.popmama.com/content-images/post/20230502/black-forest-cakes-35999b2c5523110b6bf3557f3473565b.jpg" />
        </q-carousel>
        
        <div class="q-pa-md row items-start q-gutter-md">
          <q-row class="q-col-gutter-md">
            <q-col :cols="12" :md="6">
              <q-card class="my-card" flat bordered>
                <q-img src="https://image.makewebeasy.net/makeweb/m_1920x0/rGAbosWut/DefaultData/AGS_0543_min.jpg" />

                <q-card-section>
                  <div class="text-overline text-orange-9">RASA COKLAT</div>
                  <div class="text-h5 q-mt-sm q-mb-xs">kue 1</div>
                  <div class="text-caption text-grey">
                    kue ini terbuat dari tanah
                  </div>
                  <div class="text-h6 text-bold q-mt-md">Rp 1.000.000</div>
                </q-card-section>

                <q-card-actions>
                  <q-btn flat color="primary" label="Share" />
                  <q-btn flat color="green" label="Buy" />

                  <q-space />
                </q-card-actions>
              </q-card>
            </q-col>
            
            <q-col :cols="12" :md="6">
              <q-card class="my-card" flat bordered>
                <q-img src="https://d1vbn70lmn1nqe.cloudfront.net/prod/wp-content/uploads/2023/07/24072104/Resep-Kue-Ulang-Tahun-Rumahan-Sederhana-dan-Elegan-.jpg.webp" />

                <q-card-section>
                  <div class="text-overline text-orange-9">RASA BENSIN</div>
                  <div class="text-h5 q-mt-sm q-mb-xs">kue 2</div>
                  <div class="text-caption text-grey">
                    kue ini terbuat dari bahan bakar bensin
                  </div>
                  <div class="text-h6 text-bold q-mt-md">Rp 300.000</div>
                </q-card-section>

                <q-card-actions>
                  <q-btn flat color="primary" label="Share" />
                  <q-btn flat color="green" label="Buy" />

                  <q-space />
                </q-card-actions>

                <q-slide-transition>
                  <div v-show="expanded">
                    <q-separator />
                    <q-card-section class="text-subtitle2">
                      {{ lorem }}
                    </q-card-section>
                  </div>
                </q-slide-transition>
              </q-card>
            </q-col>
            
            <q-col :cols="12" :md="6">
              <q-card class="my-card" flat bordered>
                <q-img src="https://cdn.idntimes.com/content-images/community/2024/01/1705315841922-050d7c823376e5868043b1f6ae8078e6-ba3b77672d25449256c943e3656b16ed.jpg" />

                <q-card-section>
                  <div class="text-overline text-orange-9">RASA KELAPA</div>
                  <div class="text-h5 q-mt-sm q-mb-xs">kue 3</div>
                  <div class="text-caption text-grey">
                    kue ini terbuat dari batang pohon kelapa
                  </div>
                  <div class="text-h6 text-bold q-mt-md">Rp 100.000</div>
                </q-card-section>

                <q-card-actions>
                  <q-btn flat color="primary" label="Share" />
                  <q-btn flat color="green" label="Buy" />

                  <q-space />
                </q-card-actions>

                <q-slide-transition>
                  <div v-show="expanded">
                    <q-separator />
                    <q-card-section class="text-subtitle2">
                      {{ lorem }}
                    </q-card-section>
                  </div>
                </q-slide-transition>
              </q-card>
            </q-col>
            
            <q-col :cols="12" :md="6">
              <q-card class="my-card" flat bordered>
                <q-img src="https://image.popmama.com/content-images/post/20230502/black-forest-cakes-35999b2c5523110b6bf3557f3473565b.jpg" />

                <q-card-section>
                  <div class="text-overline text-orange-9">RASA SEMEN 3 RODA</div>
                  <div class="text-h5 q-mt-sm q-mb-xs">kue 4</div>
                  <div class="text-caption text-grey">
                    kue nya terbuat dari semen 3 roda
                  </div>
                  <div class="text-h6 text-bold q-mt-md">Rp 100.000</div>
                </q-card-section>

                <q-card-actions>
                  <q-btn flat color="primary" label="Share" />
                  <q-btn flat color="green" label="Buy" />

                  <q-space />
                </q-card-actions>

                <q-slide-transition>
                  <div v-show="expanded">
                    <q-separator />
                    <q-card-section class="text-subtitle2">
                      {{ lorem }}
                    </q-card-section>
                  </div>
                </q-slide-transition>
              </q-card>
            </q-col>
            
          </q-row>
        </div>
      </q-page>
    </q-page-container>

    <q-footer elevated class="bg-pink text-white" height-hint="98">
  <q-toolbar>
    <q-toolbar-title>warung kevin</q-toolbar-title>
  </q-toolbar>
</q-footer>

  </q-layout>
</template>

<script setup>
import { ref } from 'vue'

const leftDrawerOpen = ref(false)
const rightDrawerOpen = ref(false)
const slide = ref(1)
const expanded = ref(false)
const lorem = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.'

const simple = ref([
  {
    label: 'Satisfied customers (with avatar)',
    avatar: 'https://cdn.quasar.dev/img/boy-avatar.png',
    children: [
      {
        label: 'Good food (with icon)',
        icon: 'restaurant_menu',
        children: [
          { label: 'Quality ingredients' },
          { label: 'Good recipe' }
        ]
      },
      {
        label: 'Good service (disabled node with icon)',
        icon: 'room_service',
        disabled: true,
        children: [
          { label: 'Prompt attention' },
          { label: 'Professional waiter' }
        ]
      },
      {
        label: 'Pleasant surroundings (with icon)',
        icon: 'photo',
        children: [
          {
            label: 'Happy atmosphere (with image)',
            img: 'https://cdn.quasar.dev/img/logo_calendar_128px.png'
          },
          { label: 'Good table presentation' },
          { label: 'Pleasing decor' }
        ]
      }
    ]
  }
])

const toggleLeftDrawer = () => {
  leftDrawerOpen.value = !leftDrawerOpen.value
}

const toggleRightDrawer = () => {
  rightDrawerOpen.value = !rightDrawerOpen.value
}
</script>

<style lang="sass" scoped>
.my-card
  width: 100%
  max-width: 350px
</style>
