<template>
  <form @submit.prevent="onSubmit" class="space-y-4">
    <Textinput
      label="Username"
      type="text"
      placeholder="Type your User Name"
      name="userName2"
      v-model="username"
      :error="usernameError"
      msgTooltip
    />
    <Textinput
      label="Correo electrónico"
      type="email"
      placeholder="Escriba su correo electrónico"
      name="emil2"
      v-model="email"
      :error="emailError"
      msgTooltip
    />

    <div class="text-right">
      <Button text="Submit" btnClass="btn-dark"></Button>
    </div>
  </form>
</template>
<script>
import Button from "@/components/Button";
import Textinput from "@/components/Textinput";
import { useField, useForm } from "vee-validate";
import * as yup from "yup";

export default {
  components: {
    Textinput,
    Button,
  },

  setup() {
    // Define a validation schema
    const schema = yup.object({
      email: yup.string().required().email(),
      username: yup.string().required(),
    });

    const { handleSubmit } = useForm({
      validationSchema: schema,
    });
    // No need to define rules for fields

    const { value: email, errorMessage: emailError } = useField("email");
    const { value: username, errorMessage: usernameError } =
      useField("username");

    const onSubmit = handleSubmit(() => {
      // console.warn(values.email);
    });

    return {
      email,

      emailError,
      username,
      usernameError,
      onSubmit,
    };
  },
};
</script>
<style lang="scss"></style>
