<template>
  <main class="page about-us-page">
    <header class="section-title">
      <h1>Giới Thiệu</h1>
    </header>

    <div class="section-body">
      <div class="body-left">
        <p>
          Trường mần non Đậu Đỗ House được thành lập vào tháng 1/4/2019 do một
          nhóm các nhà giáo dục tâm huyết trong lĩnh vực giáo dục trẻ kết hợp
          với hệ thống nhà hàng Tâm Chay theo phương pháp giáo dục thuận tự
          nhiên, mong muốn xây dựng một ngôi trường hạnh phúc, ở đó trẻ được an
          toàn, yêu thương, tự do sáng tạo, gần gũi với thiên nhiên.
        </p>
        <p>
          Trường Mầm non Đậu Đỗ House - Đỗ Đức Dục trả trẻ con về thế giới giao
          tiếp từ trái tim và sống chan hòa cùng tự nhiên, đưa các con về giá
          trị sống cốt lõi là sống với lòng yêu thương chan hoà. Tạo môi trường
          và được nâng đỡ, khuyến khích con vượt qua nhiều thách thức, được tôn
          trọng tự trải nghiệm để học hỏi mỗi ngày.
        </p>
        <div class="timeline">
          <div class="line l1"></div>
          <div class="dl dl1">
            <div class="line"></div>
            <div class="dot"></div>
            <div class="line"></div>
          </div>
          <div class="dl dl2">
            <div class="line"></div>
            <div class="dot"></div>
            <div class="line"></div>
          </div>
          <div class="dl dl3">
            <div class="line"></div>
            <div class="dot"></div>
            <div class="line"></div>
          </div>
          <p class="d d1">
            2020 <br />
            - <br />
            2019
          </p>
          <p class="p p1">
            Trường có 70 học sinh với 10 cán bộ nhân viên mong muốn xây dựng một
            ngôi trường hạnh phúc yêu thương thuận tự nhiên, các con được học
            hỏi khám phá theo nhịp điệu theo phương pháp giáo dục steiner kết
            hợp với các giá trị truyền thống văn hóa của dân tộc Việt Nam nuôi
            dưỡng tình yêu từ trái tim mỗi trẻ, trẻ được hòa nhập vào cuộc sống
            cùng tình yêu thiên nhiên.
          </p>
          <p class="d d2">
            2021 <br />
            - <br />2020
          </p>
          <p class="p p2">
            Trong giai đoạn này, trường đã triển khai được hoạt động đi vườn
            hàng tháng các con được ra ngoài dạo chơi với thiên nhiên, khám phá
            xúc chạm để sự trải nghiệm của trẻ như thật, nhà trường luôn cố gắng
            nỗ lực trong việc giúp trẻ được trải nghiệm, tự thân học hỏi, khám
            phá nhiều nhất có thể trong khả năng của mình. Và đưa ngoại ngữ với
            phương châm là một phương tiện học hỏi thứ 2 giúp các con hòa nhập
            với thế giới, thuận tự nhiên, các con học với giáo viên bản ngữ vui
            chơi với các vần điệu bài hát tự nhiên.
          </p>
          <p class="d d3">
            2022 <br />
            - <br />
            2021
          </p>
          <p class="p p3">
            Giai đoạn này, vừa là cơ hội vừa là thách thức với giáo dục mầm non,
            nhưng ở Đậu Đỗ House sự bình an luôn hiện hữu bằng tình yêu thương
            rộng lớn, chúng tôi đã đào tạo giáo viên bài bản hơn bởi đội ngũ
            chuyên gia tâm lý giáo dục trẻ em, đồng thời các kỹ năng chuyên môn,
            giá trị sống luôn được nâng cao, cân bằng giúp các cô mạnh mẽ, vững
            vàng an nhiên từ trong nội tâm.
          </p>
        </div>
      </div>
      <div class="body-right">
        <img
          loading="lazy"
          class="figure-hover-animation"
          src="~assets/images/hb-medium.webp"
        />
      </div>
    </div>
  </main>
</template>

<script>
export default {
  data() {
    return {
      title: 'Giới Thiệu Đậu Đỗ House',
      description:
        'Trường Mầm non Đậu Đỗ House - Đỗ Đức Dục trả trẻ con về thế giới giao tiếp từ trái tim và sống chan hòa cùng tự nhiên, đưa các con về giá trị sống cốt lõi là sống với lòng yêu thương chan hoà. Tạo môi trường và được nâng đỡ, khuyến khích con vượt qua nhiều thách thức, được tôn trọng tự trải nghiệm để học hỏi mỗi ngày.',
    }
  },
  head() {
    return {
      title: this.title,
      description: this.description,
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: this.description,
        },
        {
          hid: 'og:title',
          name: 'og:title',
          content: this.title,
        },
        {
          hid: 'og:description',
          name: 'og:description',
          content: this.description,
        },
        {
          hid: 'og:url',
          name: 'og:url',
          content: `https://daudohouse.com/gioi-thieu`,
        },
      ],
    }
  },
}
</script>

<style></style>
