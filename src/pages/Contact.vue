<template>
  <v-row class="ma-4 d-flex justify-center">
    <v-col cols="12" class="mt-12">
      <span class="d-flex justify-center"
        >new player looking for more info?
        <a
          style="color: #092062"
          href="https://drive.google.com/file/d/1CqQQONaCDBtOOluxSETrnha3UhLZovJN/view"
          target="_blank"
          rel="noopener noreferrer"
        >
          click here
        </a>
        <br /></span
    ></v-col>

    <!-- Contact Us Form Column (4 columns width on medium screens, full width on smaller screens) -->
    <v-col cols="12" md="3">
      <v-card variant="default" width="100%">
        <v-card-title class="d-flex justify-center">contact us!</v-card-title>

        <form @submit.prevent="sendEmail">
          <v-text-field
            v-model="userName"
            placeholder="Your Name"
            variant="outlined"
            required
            width="100%"
          />
          <v-text-field
            v-model="userEmail"
            placeholder="Your Email"
            variant="outlined"
            required
            width="100%"
          />
          <v-textarea
            v-model="userMessage"
            placeholder="Message"
            variant="outlined"
            required
            width="100%"
          />
          <v-btn class="float-right mr-2" variant="outlined">
            <span style="color: #ffffff" class="text-lowercase"
              >Submit</span
            ></v-btn
          >
        </form>
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
