<template>
  <div class="grid lg:grid-cols-3 md:grid-cols-2 grid-cols-1 gap-5">
    <Textinput
      label="Full name"
      name="hmi_Fullname"
      type="text"
      placeholder="Full name"
    />
    <Textinput
      label="Correo electrónico"
      name="hmi_email"
      type="email"
      placeholder="Escriba su correo electrónico"
    />
    <Textinput
      label="Phone"
      name="hmi_phone"
      type="phone"
      placeholder="Escriba su correo electrónico"
    />
    <Textinput
      label="Password"
      name="hmi_password"
      type="Password"
      placeholder="8+ characters, 1 capitat letter "
    />
    <Textinput
      label="Company"
      name="hmi_commpanyname"
      type="text"
      placeholder="Company name"
    />
    <Select label="Country" name="hmi_country" />
    <div class="space-y-5">
      <Checkbox label="Remember me" />
      <Button text="Submit" btnClass="btn-dark" />
    </div>
  </div>
</template>
<script>
import Textinput from "@/components/Textinput";
import Checkbox from "@/components/Checkbox";
import Button from "@/components/Button";
import Select from "@/components/Select";

export default {
  components: {
    Textinput,
    Checkbox,
    Button,
    Select,
  },
};
</script>
<style lang=""></style>
