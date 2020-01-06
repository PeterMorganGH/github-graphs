<template>
  <div class="container">
    <div class="row">
      <div class="col">
        <h1 class="text-center text-white font-weight-bold my-4 py-5">
          Generate a graph
        </h1>
      </div>
    </div>
    <div class="row align-items-stretch">
      <div class="col-lg-4 mb-4">
        <div class="card h-100 shadow py-3">
          <div class="card-body">
            <svg
              class="my-3"
              width="37"
              height="38"
              viewBox="0 0 37 38"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M18.172 0.946228C8.14108 0.946228 0 9.0873 0 19.1183C0 29.1492 8.14108 37.2903 18.172 37.2903C28.203 37.2903 36.3441 29.1492 36.3441 19.1183C36.3441 9.0873 28.203 0.946228 18.172 0.946228ZM18.172 6.39784C21.1886 6.39784 23.6237 8.83289 23.6237 11.8495C23.6237 14.866 21.1886 17.3011 18.172 17.3011C15.1555 17.3011 12.7204 14.866 12.7204 11.8495C12.7204 8.83289 15.1555 6.39784 18.172 6.39784ZM18.172 32.2021C16.0129 32.2022 13.8874 31.6678 11.985 30.6469C10.0825 29.6259 8.46232 28.15 7.26882 26.3507C7.32333 22.7345 14.5376 20.7538 18.172 20.7538C21.7883 20.7538 29.0208 22.7345 29.0753 26.3507C27.8818 28.15 26.2616 29.6259 24.3591 30.6469C22.4567 31.6678 20.3311 32.2022 18.172 32.2021Z"
                fill="#1074E7"
              />
            </svg>
            <h2 class="h4 my-4 font-weight-bold">Interactive Friends Chart</h2>
            <p class="card-text">
              Creates a web chart of the selected user and both their followers
              and anyone they are following themselves.
            </p>
          </div>
          <div class="card-footer bg-transparent border-top-0">
            <div class="input-group input-group-lg">
              <input
                id="input-friends-graph"
                type="text"
                class="form-control"
                placeholder="Username"
                v-model="friendsInput"
              />
              <div class="input-group-append">
                <a
                  class="btn btn-primary"
                  :href="`/friends-graph/${friendsInput}`"
                  >Generate</a
                >
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="col-lg-4 mb-4">
        <div class="card h-100 shadow py-3">
          <div class="card-body">
            <svg
              class="my-3"
              width="36"
              height="36"
              viewBox="0 0 36 36"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M0 0H3.6V32.4H36V36H0V0ZM9 14.4H27V19.8H9V14.4ZM16.2 23.4H34.2V28.8H16.2V23.4ZM7.2 3.6H36V10.8H32.4V7.2H10.8V10.8H7.2V3.6Z"
                fill="#1074E7"
              />
            </svg>
            <h2 class="h4 my-4 font-weight-bold">Repo Timeline</h2>
            <p class="card-text">
              Displays a timeline of every repo belonging to the selected user
              in chronological order, along with information pertaining to each
              repo.
            </p>
          </div>
          <div class="card-footer bg-transparent border-top-0">
            <div class="input-group input-group-lg">
              <input
                id="input-timeline-graph"
                type="text"
                class="form-control"
                placeholder="Username"
                v-model="timelineInput"
              />
              <div class="input-group-append">
                <a
                  class="btn btn-primary"
                  :href="`/timeline-graph/${timelineInput}`"
                  >Generate</a
                >
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="col-lg-4 mb-4">
        <div class="card h-100 shadow py-3">
          <div class="card-body">
            <svg
              class="my-3"
              width="37"
              height="31"
              viewBox="0 0 37 31"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M0 31V11C0 10.5093 0.19491 10.0388 0.541852 9.69185C0.888795 9.34491 1.35935 9.15 1.85 9.15H9.25V2C9.25 0.895432 10.1454 0 11.25 0H25.75C26.8546 0 27.75 0.89543 27.75 2V9.15H35.15C35.6407 9.15 36.1112 9.34491 36.4581 9.69185C36.8051 10.0388 37 10.5093 37 11V31H22.2V21.75H14.8V31H0ZM14.8 3.5V8.8H22.2V3.5H14.8ZM3.7 27.3H11.1V21.75H3.7V27.3ZM3.7 18.05H11.1V12.5H3.7V18.05ZM25.9 27.3H33.3V21.75H25.9V27.3ZM25.9 18.05H33.3V12.5H25.9V18.05ZM14.8 18.05H22.2V12.5H14.8V18.05Z"
                fill="#1074E7"
              />
            </svg>

            <h2 class="h4 my-4 font-weight-bold">
              Interactive Organization Chart
            </h2>
            <p class="card-text">
              Creates a web chart of the specified organization and all
              associated repos.
            </p>
          </div>
          <div class="card-footer bg-transparent border-top-0">
            <div class="input-group input-group-lg">
              <input
                id="input-organization-graph"
                type="text"
                class="form-control"
                placeholder="Organization"
                v-model="orgInput"
              />
              <div class="input-group-append">
                <a class="btn btn-primary" :href="`/org-repo-graph/${orgInput}`"
                  >Generate</a
                >
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      friendsInput: "",
      timelineInput: "",
      orgInput: ""
    };
  }
};
</script>
