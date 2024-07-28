<template>
  <b-container class="mt-5">
    <h6 class="pt-2">Confirmation</h6>
    <b-row>
      <b-col  class="d-flex justify-content-between">
        <div>
          <div class="card ">
            <b-card title="Details" sub-title="Card subtitle">
              <div class="d-flex justify-content-between ">
                <b-card-text>Start Date</b-card-text>
                <b-card-text>Amount of students selected</b-card-text>
              </div>
              <div class="d-flex justify-content-between ">

                <p>{{ startDate }}</p>
                <p>{{ studentCount }}</p>
              </div>
            </b-card>
          </div>
          <div class="mt-5">
            <b-card>
              <p>Selected Students</p>
              <b-row>
                <b-col cols="12" v-for="student in students" :key="student.id" class="mb-2">
                  <div class="d-flex align-items-center">
                    <img :src="student.imgSrc" alt="Student Image" class="student-image rounded-circle mr-2">
                    <p class="mb-0 mr-2 ">{{ student.name }}</p>
                  </div>
                </b-col>
              </b-row>
            </b-card>
          </div>
        </div>
        <div>
  <b-card
    tag="article"
    style="max-width: 20rem;"
    class="mb-2  "
    rounded
    
  >
  <div class="text-center mb-2">

    <img src="https://picsum.photos/600/300/?image=25" alt="Image"  class="rounded custom-img">
  </div>
  <b-card-title class="mt-2">Finance</b-card-title>
    <b-card-text>
      Gear up to master the essential skills for the future
    </b-card-text>
    <p class="text-color">8 Lessons</p>
    <b-card-title>Description</b-card-title>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Possimus excepturi soluta laboriosam fuga aspernatur beatae commodi et quae distinctio optio ad nisi, vitae, consectetur autem. Aliquid id iste omnis maxime!</p>
  </b-card>
</div>
      </b-col>
    </b-row>
    <div class="text-end mb-2">
      <b-button class="text-color white px-5 ">Back</b-button>
      <b-button class="text-white pink px-5">Continue</b-button>
    </div>
  </b-container>
</template>

<script>


export default {
  name: 'App',
  data() {
    return {
      startDate: '2024-07-28',
      studentCount: 25,
      students: [
        { id: 1, name: 'Student 1', imgSrc: 'https://via.placeholder.com/50', selected: false },
        { id: 2, name: 'Student 2', imgSrc: 'https://via.placeholder.com/50', selected: false },
        { id: 3, name: 'Student 3', imgSrc: 'https://via.placeholder.com/50', selected: false },
        { id: 4, name: 'Student 4', imgSrc: 'https://via.placeholder.com/50', selected: false },
        { id: 5, name: 'Student 5', imgSrc: 'https://via.placeholder.com/50', selected: false },
        { id: 6, name: 'Student 6', imgSrc: 'https://via.placeholder.com/50', selected: false },
        { id: 7, name: 'Student 7', imgSrc: 'https://via.placeholder.com/50', selected: false },
        { id: 8, name: 'Student 8', imgSrc: 'https://via.placeholder.com/50', selected: false }
      ],
    };
  }
};
</script>

<style>
.container {
  background-color: rgba(237, 233, 233, 0.877)
}

.card {
  width: 50rem;
}

.student-image {
  border: 2px solid rgb(249, 173, 185);
  width: 50px;
  height: 50px;
  margin-right: 10px;
}

.text-color {
  color: rgb(254, 25, 109) !important
}

.pink {
  background-color: rgb(254, 25, 109) !important;
  border-color: rgb(254, 25, 109) !important;
  border-radius: 25px !important;
}

.white {
  background-color: white !important;
  border-color: rgb(254, 25, 109) !important;
  border-radius: 25px !important;
  margin-right: 10px
}
.custom-img{
  width:75%;
  height:75%
}
</style>
