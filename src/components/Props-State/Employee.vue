<template>
<div class="container">
    <div class="row">
        <div class="col">
            <p class="h3 text-danger">Employee</p>
            <ul class="list-group">
                <li class="list-group-item">
                    Name : {{employee.name}}
                </li>
                <li class="list-group-item">
                    Age : {{employee.age}}
                </li>
                <li class="list-group-item">
                    Designation : {{employee.designation}}
                </li>
            </ul>
        </div>
    </div>
</div>
</template>

<script>
export default {
  name: "Employee-vue",
  data() {
      return {
          employee: {
              name: "Sodiq",
              age: 23,
              designation: "Web Dev"
          }
      }
  }

};
</script>

<style></style>
