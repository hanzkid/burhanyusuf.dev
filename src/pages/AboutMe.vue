<template>
  <Layout :show-logo="false">
    <!-- Author intro -->
    <Author :show-title="true" />

    <div class="post-card content-box" style="padding-top: 1rem;">
        <div class="post-card__content">
            <h2 class="post-card__title">Tentang Saya</h2>
            <p class="post-card__description">
                Sejak kecil, saya selalu menyukai sesuatu yang mempunyai 'pattern' , pola, dan sesuatu yang memiliki nilai pasti.
                Sebelum mengenal pemrograman, awalnya saya menyukai matematika, science, astronomi dan sebagainya.
                Saat kelas 5 sd, saya mempunyai sebuah komputer dengan processor Intel Pentium 3. Pada saat itulah saya mulai sedikit tertarik dengan dunia komputer.
                Fokus pada dunia pemrograman mulai dari sekitar kelas 3 smk kemudian dilanjutkan dengan kuliah program studi IT.
            </p>
            <p>
                Selama masa kuliah, mengambil beberapa pekerjaan parttime maupun fulltime dan project sebagai freelance. Beberapa project yang dibuat adalah :
            </p>
               <ul>
                    <li>CBT untuk Ujian Semester / Ujian Sekolah pada SMK Wilayah Jakarta Pusat 2</li>
                    <li>CBT Distributed System Sekolah pada SMK Wilayah Jakarta Pusat 2</li>
                    <li>Sistem Sertifikasi Untuk LSP KFI</li>
                    <li>Sistem Sertifikasi Untuk LSP PHC</li>
                    <li>Beberapa Website Sekolah</li>
                </ul>
            <p>
                Saat ini sedang mengikuti program bootcamp FullStack JavaScript yang diadakan oleh Hacktiv8. Program ini memakan waktu pembelajaran selama 4 bulan.

            </p>
        </div>
    </div>

  </Layout>
</template>

<script>
import Author from '~/components/Author.vue'

export default {
  components: {
    Author
    },
  metaInfo: {
    title: 'Hello, world!'
  }
}
</script>
