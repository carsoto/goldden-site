<template>
  <div class="space-y-4">
    <Textinput
      label="Full name"
      name="v_Fullname"
      type="text"
      placeholder="Full name"
    />
    <Textinput
      label="Correo electrónico"
      name="v_email"
      type="email"
      placeholder="Escriba su correo electrónico"
    />
    <Textinput
      label="Phone"
      name="v_phone"
      type="phone"
      placeholder="Escriba su correo electrónico"
    />
    <Textinput
      label="Password"
      name="v_password"
      type="Password"
      placeholder="8+ characters, 1 capitat letter "
    />
    <Checkbox label="Remember me" />
    <Button text="Submit" btnClass="btn-dark" />
  </div>
</template>
<script>
import Textinput from "@/components/Textinput";
import Checkbox from "@/components/Checkbox";
import Button from "@/components/Button";

export default {
  components: {
    Textinput,
    Checkbox,
    Button,
  },
};
</script>
<style lang=""></style>
