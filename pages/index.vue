<template>
  <img src="/assets/img/bg.jpeg" alt="" width="100%" />
  <div class="container">
    <div class="row">
      <h1 class="text-center mt-5">Sambutan Kepala Sekolah</h1>
      <div class="clearfix">
        <img
          src="assets/img/kepsek.jpg"
          class="col-md-3 float-md-end mb-3"
          alt="..."
        />
        <p>
          Assalamualaikum Warahmatullahi Wabarakatuh<br />
          Selamat datang di SMKN 4 Tasikmalaya. Segala puji dan syukur kita
          panjatkan kehadirat Allah SWT, semoga kita semua ada dalam
          lindungan-Nya. Dan atas perkenan-Nya pula kami dapat menghadirkan
          website SMK Negeri 4 Tasikmalaya ini. Kami berharap dengan adanya
          website di SMK Negeri 4 Tasikmalaya ini para pengunjung dapat mengenal
          lebih jauh tentang sekolah kami sehingga dapat mempererat tali
          silaturrahmi antara sekolah dengan masyarakat demi kemajuan kita
          bersama. Tiada gading yang tak retak, website kami ini masih dalam
          proses pengembangan, masih banyak kekurangan yang harus kami perbaiki.
          Kritik dan sarannya yang membangun sangat kami harapkan untuk
          pengembangan ke depan. Akhirnya, saya mengucapkan terimakasih yang
          sebesar-besarnya kepada semua pihak yang tidak dapat disebutkan satu
          segala bantuan dan persatu atas fasilitasnya yang telah diberikan
          semoga semua yang kita lakukan bermanfaat bagi masyarakat.
          <br />Wassalamu'alaikum Warahmatullahi Wabarakatuh.
        </p>
      </div>

      <div class="container py-5">
        <h3 class="text-center pb-3">Berita</h3>
        <div class="row">
          <div
            v-for="(get, i) in berita"
            :key="i"
            class="card col-md"
            style="width: 18rem"
          >
            <img :src="get.poto" class="card-img-top" alt="..." />
            <div class="card-body">
              <p class="card-text">
                {{ get.nama }}
              </p>
            </div>
          </div>
        </div>
      </div>

      <h3 class="text-center">Kompetensi Keahlian</h3>
      <div class="row my-5">
        <!-- PPLG -->
        <div class="row align-items-center mb-4 justify-content-center">
          <div class="col-md-2 text-center">
            <img
              src="assets/img/rpl.jpg"
              alt="PPLG"
              class="img-fluid rounded"
            />
          </div>
          <div class="col-md-6">
            <h5 class="card-title text-center text-md-start">
              Pengembangan Perangkat Lunak Dan Gim (PPLG)
            </h5>
          </div>
        </div>

        <!-- TJKT -->
        <div class="row align-items-center mb-4 justify-content-center">
          <div class="col-md-2 text-center">
            <img
              src="assets/img/tjkt.jpg"
              alt="TJKT"
              class="img-fluid rounded"
            />
          </div>
          <div class="col-md-6">
            <h5 class="card-title text-center text-md-start">
              Teknik Jaringan Komputer Dan Telekomunikasi
            </h5>
          </div>
        </div>
        <!-- TBSM -->
        <div class="row align-items-center mb-4 justify-content-center">
          <div class="col-md-2 text-center">
            <img
              src="assets/img/tbsm.jpg"
              alt="TBSM"
              class="img-fluid rounded"
            />
          </div>
          <div class="col-md-6">
            <h5 class="card-title text-center text-md-start">
              Teknik Dan Bisnis Sepeda Motor
            </h5>
          </div>
        </div>
        <!-- DKV -->
        <div class="row align-items-center mb-4 justify-content-center">
          <div class="col-md-2 text-center">
            <img
              src="assets/img/dkv.jpg"
              alt="TBSM"
              class="img-fluid rounded"
            />
          </div>
          <div class="col-md-6">
            <h5 class="card-title text-center text-md-start">
              Desain Komunikasi Komputer
            </h5>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const supabase = useSupabaseClient();

const berita = ref([]);

const getData = async () => {
  const { data } = await supabase.from("berita").select(`*`);
  if (data) berita.value = data;
};

onMounted(() => {
  getData();
});
</script>
