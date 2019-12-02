<template>
    <div id="app">
        <!-- <div>
      <BaseTextInput v-model="msg" placeholder="hahha"></BaseTextInput>
      <br>
      <CustomCheckbox v-model="checkedBox" label="checkbox1"></CustomCheckbox>
      <CustomCheckbox v-model="otherCheckedBox" label="checkbox2"></CustomCheckbox>
      <br>
      <CustomRadio v-model="checkedRadio" name="base" label="male" value="on"></CustomRadio>
      <CustomRadio v-model="checkedRadio" name="base" label="female" value="off"></CustomRadio>
      <br>
      <CustomSelect v-model="selected" :list="obj"></CustomSelect>
    </div>
    <hr>
    <NavigationLink>your profile</NavigationLink>
    <br>
    <SubmitButton>Save</SubmitButton>
    <br>
    <BaseLayout>
      <template v-slot:header>
        <h1>Here might be a page title</h1>
      </template>
      <template v-slot:default>
        <p>A paragraph for the main content.</p>
        <p>And another one.</p>
      </template>
      <template v-slot:footer>
        <p>Here's some contact info</p>
      </template>
        </BaseLayout>-->
        <currentUser>
            <template #lastname="{obj}">{{obj.lastName}}</template>
            <template #firstname="{obj}">{{obj.firstName}}</template>
            <template #default="{usr={name: 'xiaowusang'}}">{{usr.name}}</template>
        </currentUser>
    </div>
</template>

<script>
import BaseTextInput from "./components/BaseTextInput.vue";
import CustomCheckbox from "./components/CustomCheckbox.vue";
import CustomRadio from "./components/CustomRadio.vue";
import CustomSelect from "./components/CustomSelect.vue";
import NavigationLink from "./components/NavigationLink.vue";
import SubmitButton from "./components/SubmitButton.vue";
import BaseLayout from "./components/BaseLayout.vue";
import currentUser from "./components/currentUser.vue";

export default {
    name: "App",
    components: {
        BaseTextInput,
        CustomCheckbox,
        CustomRadio,
        CustomSelect,
        NavigationLink,
        SubmitButton,
        BaseLayout,
        currentUser
    },
    data() {
        return {
            msg: "",
            checkedBox: false,
            otherCheckedBox: false,
            checkedRadio: true,
            selected: "",
            obj: [
                { name: "bily", age: 18 },
                { name: "lily", age: 18 },
                { name: "smith", age: 17 }
            ]
        };
    }
};
</script>

<style>
</style>
