<template>
  <form @submit.prevent="onSubmit" class="space-y-4">
    <Textinput
      label="Correo electrónico"
      type="email"
      placeholder="Escriba su correo electrónico"
      name="emil"
      v-model="email"
      :error="emailError"
      classInput="h-[48px]"
    />

    <button type="submit" class="btn btn-dark block w-full text-center">
      Enviar correo electrónico de recuperación
    </button>
  </form>
</template>
<script>
import Textinput from "@/components/Textinput";
import { useField, useForm } from "vee-validate";
import * as yup from "yup";

export default {
  components: {
    Textinput,
  },
  data() {
    return {
      checkbox: false,
    };
  },
  setup() {
    // Define a validation schema
    const schema = yup.object({
      email: yup.string().required().email(),
    });

    const { handleSubmit } = useForm({
      validationSchema: schema,
    });
    // No need to define rules for fields

    const { value: email, errorMessage: emailError } = useField("email");

    const onSubmit = handleSubmit(() => {
      // console.warn(values);
    });

    return {
      email,
      emailError,
      onSubmit,
    };
  },
};
</script>
<style lang="scss"></style>
