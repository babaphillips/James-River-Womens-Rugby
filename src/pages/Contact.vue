<template>
  <!-- Row with Contact Us on the left, spacing, and JRW Board on the right -->
  <v-row class="d-flex justify-space-evenly ma-4">
    <!-- Contact Us Form Column (4 columns width on medium screens, full width on smaller screens) -->
    <v-col cols="12" md="3">
      <v-card
        class="bg-white"
        variant="outlined"
        elevation="10"
        width="100%"
        style="border-color: #092062; border-width: 2px"
      >
        <v-card-title
          class="ma-4 text-overline textConfig d-flex justify-center"
          >Contact Us!</v-card-title
        >

        <form @submit.prevent="sendEmail">
          <v-text-field
            v-model="userName"
            placeholder="Your Name"
            variant="outlined"
            color="green"
            required
            width="100%"
            class="pa-2"
          />
          <v-text-field
            v-model="userEmail"
            placeholder="Your Email"
            variant="outlined"
            required
            color="green"
            width="100%"
            class="pa-2"
          />
          <v-textarea
            v-model="userMessage"
            placeholder="Message"
            variant="outlined"
            color="green"
            required
            width="100%"
            class="pa-2"
          />
          <v-btn class="float-right mb-2 mr-2" variant="tonal">
            <span class="text-white">Submit</span></v-btn
          >
        </form>
      </v-card>
    </v-col>

    <!-- Board Members Column (7 columns width on medium screens, full width on smaller screens) -->
    <v-col cols="12" md="9" class="d-flex justify-center">
      <v-card
        class="bg-white"
        variant="outlined"
        elevation="10"
        style="border-color: #092062; border-width: 2px"
      >
        <v-card-title class="ma-4 text-overline textConfig text-center">
          The 2024 JRW Board
        </v-card-title>

        <v-row class="d-flex justify-center mb-4">
          <!-- Loop through board members -->
          <v-col
            v-for="(member, index) in boardMembers"
            :key="index"
            cols="12"
            sm="6"
            md="3"
            class="d-flex justify-center"
          >
            <v-card
              class="text-center board-card bg-white"
              variant="outlined"
              height="200px"
              width="250px"
            >
              <!-- Profile Image -->
              <v-img
                :src="member.photo"
                class="mx-auto mt-4"
                height="70px"
                width="70px"
                contain
                rounded
              />
              <v-card-title>{{ member.name }}</v-card-title>
              <v-card-subtitle>{{ member.role }}</v-card-subtitle>
              <v-card-subtitle>
                <a class="text-black" :href="'mailto:' + member.email">
                  {{ member.email }}
                </a>
              </v-card-subtitle>
            </v-card>
          </v-col>
        </v-row>
      </v-card>
    </v-col>
  </v-row>
</template>

<script setup>
import { ref } from "vue";
import emailjs from "emailjs-com";
import { useToast } from "vue-toastification";

// Declare reactive references for userName, userEmail, and userMessage
const userName = ref("");
const userEmail = ref("");
const userMessage = ref("");

// Initialize Toast
const toast = useToast();

// Board Members Data
const boardMembers = ref([
  {
    name: "Emily Yanuskiewicz",
    role: "President",
    email: "president@jamesriverrugby.com",
    photo: "path/to/photo1.jpg",
  },
  {
    name: "Sonya Richard",
    role: "Vice President",
    email: "vp@jamesriverrugby.com",
    photo: "path/to/photo2.jpg",
  },
  {
    name: "Vicky Whydell",
    role: "Match Secretary",
    email: "matchsec@jamesriverrugby.com",
    photo: "path/to/photo3.jpg",
  },
  {
    name: "Grapes McElroy",
    role: "Treasurer",
    email: "finance@jamesriverrugby.com",
    photo: "path/to/photo4.jpg",
  },
  {
    name: "Callie Pace",
    role: "Secretary",
    email: "teamsec@jamesriverrugby.com",
    photo: "path/to/photo5.jpg",
  },
  {
    name: "Jane Duncan",
    role: "Recruitment Chair",
    email: "signup2play@jamesriverrugby.com",
    photo: "path/to/photo9.jpg",
  },
  {
    name: "Elle Smith",
    role: "Social Chair",
    email: "socials@jamesriverrugby.com",
    photo: "path/to/photo9.jpg",
  },
  {
    name: "Trei Young",
    role: "Diversity & Cultural Ambassador",
    email: "diversity@jamesriverrugby.com",
    photo: "path/to/photo9.jpg",
  },
  {
    name: "Fox Clemmer",
    role: "Member at Large",
    email: "teamrep@jamesriverrugby.com",
    photo: "path/to/photo10.jpg",
  },
  {
    name: "Tim",
    role: "Head Coach",
    email: "teamrep@jamesriverrugby.com",
    photo: "path/to/photo10.jpg",
  },
]);

// Function to send email using EmailJS
const sendEmail = () => {
  const templateParams = {
    user_name: userName.value,
    user_email: userEmail.value,
    user_message: userMessage.value,
  };

  // Use the emailjs.send method to send the email
  emailjs
    .send(
      "service_s6lzi4d",
      "template_e6jwrwi",
      templateParams,
      "W2NYk-om8LxJ5nEWT"
    )
    .then((response) => {
      // Reset the form fields
      userName.value = "";
      userEmail.value = "";
      userMessage.value = "";

      // Show success toast notification
      toast.success("Your message has been sent successfully!");
    })
    .catch((error) => {
      // Show error toast notification
      toast.error("Something went wrong. Please try again.");
    });
};
</script>

<style scoped>
/* Ensure all cards are the same height */
.board-card {
  height: 300px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

/* Styling adjustments to ensure consistency */
.v-card-title,
.v-card-subtitle {
  padding: 0 10px;
  margin-bottom: 10px;
}

.v-btn {
  padding: 5px 20px;
  background-color: #029345;
}

.v-img {
  border-radius: 50%; /* Make the image round */
  overflow: hidden;
}

.textConfig {
  font-size: 1.8rem !important;
  font-weight: 650;
  color: #029345;
}
</style>
