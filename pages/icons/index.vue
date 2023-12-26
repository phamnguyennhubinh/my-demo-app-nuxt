<template>
  <div>
    <light-table :items="items"/>
  </div>
</template>

<script>
export default {
  name: "IconPage",
  layout: "DefaultLayout",
  data() {
    const items = [
      {
        project: "Argon Design System",
        budget: "$2500 USD",
        status: "• pending",
        users: "",
        completion: "60%",
      },
      {
        project: "Angular Now UI Kit PRO",
        budget: "$3150 USD",
        status: "• completed",
        users: "",
        completion: "72%",
      },
      {
        project: "Angular Now UI Kit PRO",
        budget: "$3150 USD",
        status: "• completed",
        users: "",
        completion: "72%",
      },
      {
        project: "Angular Now UI Kit PRO",
        budget: "$3150 USD",
        status: "• completed",
        users: "",
        completion: "72%",
      },
      {
        project: "Angular Now UI Kit PRO",
        budget: "$3150 USD",
        status: "• completed",
        users: "",
        completion: "72%",
      },
      {
        project: "Angular Now UI Kit PRO",
        budget: "$3150 USD",
        status: "• completed",
        users: "",
        completion: "72%",
      },
      {
        project: "Black Dashboard",
        budget: "$1800 USD",
        status: "• delayed",
        users: "",
        completion: "60%",
      },
      {
        project: "React Material Dashboard",
        budget: "$4400 USD",
        status: "• on schedule",
        users: "",
        completion: "90%",
      },
      {
        project: "Vue Paper UI Kit PRO",
        budget: "$2200 USD",
        status: "• completed",
        users: "",
        completion: "100%",
      },
      {
        project: "Argon Design System",
        budget: "$2500 USD",
        status: "• pending",
        users: "",
        completion: "60%",
      },
      {
        project: "Angular Now UI Kit PRO",
        budget: "$1800 USD",
        status: "• completed",
        users: "",
        completion: "100%",
      },
      {
        project: "Black Dashboard",
        budget: "$3150 USD",
        status: "• delayed",
        users: "",
        completion: "72%",
      },
      {
        project: "Vue Paper UI Kit PRO",
        budget: "$2200 USD",
        status: "• completed",
        users: "",
        completion: "100%",
      },
    ];
    return {
      items,
    };
  },
};
</script>
