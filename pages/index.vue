<template>
  <div class="relative">
    <div class="h-screen">
      <div class="flex flex-col">
        <!-- 
          Header Content ( Landing Page )

          PARAMETERS
          :imgURL (URL for Background)
          :header_txt ( Header Text )
          :second_header ( Header 2 Text)
          :descriptions ( Descriptions )
        -->
        <HeaderContent
          imgURL="https://res.cloudinary.com/grohealth/image/upload/f_auto,fl_lossy,q_auto/v1581688713/DCUK/Content/iStock-938993594-1000x600.jpg"
          header_txt="Coffee Mou"
          second_header="Aroma feeling"
          descriptions="FullStack Web Development Hands on"
        ></HeaderContent>
        <!-- 
          About Content 

          PARAMETERS
          :imgURL ( URL for about us )
        -->
        <AboutContent
          imgURL="https://www.terbodorecoffee.co.za/wp-content/uploads/2018/08/about-us-1.jpg"
        >
          <template v-slot:about>Coffee Mou is a coffee shop that serves good coffee to everyone.</template>
        </AboutContent>

        <ServiceContent>
          <template v-slot:services>
            <!-- 

              Service 

              PARAMETERS

              :imgURL (image url)
            -->
            <Service imgURL="/img/icon1.png" title="Own Combination of Coffee">
              <template
                v-slot:content
              >Order your own favourite coffee accoding to your own preference!</template>
            </Service>

            <Service imgURL="/img/icon2.png" title="Latte?">
              <template v-slot:content>Do you want a cup of latte?</template>
            </Service>

            <Service imgURL="/img/icon3.png" title="Mocha?">
              <template v-slot:content>Do you want a cup of Mocha?</template>
            </Service>

            <Service imgURL="/img/icon4.png" title="Cappucino?">
              <template v-slot:content>Do you want a cup of Cappucino?</template>
            </Service>
          </template>
        </ServiceContent>

        <!-- 
          Portfolio
        -->
        <PortfolioContent>
          <template v-slot:portfolio>
            <!-- 
              Project

              PARAMETERS
              :imgURL ( img URL for Project )
              :name ( Name of the Project )
              :project ( Name of Project Type)
              :projectURL ( Link Address to project)
            -->
            <Project
              imgURL="https://og.github.com/octocat/github-octocat@1200x630.png"
              name="GitHub Account"
              project="NuxtJS"
              projectURL="https://github.com/1511KC/company-template"
            />

            <Project
              imgURL="https://imageog.flaticon.com/icons/png/512/174/174857.png?size=1200x630f&pad=10,10,10,10&ext=png&bg=FFFFFFFF"
              name="Linkedin Account"
              project="Linkedin"
              projectURL="https://www.linkedin.com/in/tan-kar-cheng-81744b16b/"
            />
          </template>
        </PortfolioContent>
        <ContactContent
          address="245, Batu 11, Desa Aman"
          email="eugune_1511@hotmail.com"
          phone="6016-985 1595"
          imgURL="https://dynaimage.cdn.cnn.com/cnn/c_fill,g_auto,w_1200,h_675,ar_16:9/https%3A%2F%2Fcdn.cnn.com%2Fcnnnext%2Fdam%2Fassets%2F150929101049-black-coffee-stock.jpg"
        />
      </div>
    </div>
  </div>
</template>
<script>
export default {
  head() {
    return {
      title: "Coffee Mou"
    };
  }
};
</script>