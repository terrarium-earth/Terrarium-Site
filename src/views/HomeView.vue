<template>
  <div class="home">
    <div class="home-header">
      <p class="title">Terrarium</p>
      <p class="subtitle">Making exciting Minecraft content!</p>
      <p class="text">
        We are a community of Minecraft mod developers and content creators
        dedicated to creating a better Minecraft experience for everyone. We're
        working on a variety of the communities favorite mods, including
        Chipped, Spirit & Ad Astra!
      </p>
      <div class="downloads">
        <a href="https://modrinth.com/user/Terrarium" class="no-animation">
          <img
            alt="modrinth"
            class="platform"
            src="https://raw.githubusercontent.com/modrinth/art/a05e2307b42762d64a370a3cf3e8b6b30735dce1/Branding/Wordmark/wordmark-dark.svg"
          />
        </a>
        <a
          href="https://www.curseforge.com/members/terrariumearth/projects"
          class="no-animation"
        >
          <img
            alt="curseforge"
            class="platform curseforge"
            src="https://www.userlogos.org/files/curseforge.png"
          />
        </a>
      </div>
    </div>
    <img
      class="home-banner-img"
      src="@/assets/home.png"
      alt="Home Page Banner Image"
    />
  </div>
  <div class="stats-banner">
    <div class="stats-content">
      <StatComponent title="22,000,000+" subtitle="Total Downloads" />
      <StatComponent title="10,000+" subtitle="Assets Made" />
      <StatComponent :title="members" subtitle="Discord Members" />
      <StatComponent title="12" subtitle="Projects Published" />
    </div>
  </div>
  <div>
    <h1 class="project-section-title">Creating Minecraft Mods</h1>
  </div>
  <div>
    <p></p>
  </div>
</template>

<script>
import StatComponent from "@/components/StatComponent";
export default {
  components: { StatComponent },
  data() {
    return {
      members: "...",
    };
  },
  mounted() {
    fetch("https://discord.com/api/v10/invites/terrarium?with_counts=true")
      .then((response) => response.json())
      .then((data) => data.approximate_member_count)
      .then((count) => {
        this.members = count.toString();
      });
  },
};
</script>

<style>
.home {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  margin: 0;
}

.home-header {
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin: 0;
  width: min-content;
}

.title {
  font-size: var(--title-font-size);
  font-family: var(--primary-font);
  margin: 0 0 24px;
  padding: 0;
}

.subtitle {
  font-size: var(--subtitle-font-size);
  font-family: var(--secondary-font);
  text-align: justify;
  margin: 0;
  color: #4a7263;
  font-weight: bold;
}

.text {
  font-size: var(--text-font-size);
  font-family: var(--secondary-font);
  text-align: justify;
  margin: 0;
  color: #4b4b4b;
}

.home-banner-img {
  object-fit: contain;
  width: 40vw;
  aspect-ratio: 1/1;
}

.downloads {
  display: flex;
  flex-direction: row;
  justify-content: left;
  margin: 0;
  margin-top: 32px;
}

/* no stretch */
.platform {
  margin: 0;
  padding: 8px 16px 8px 16px;
  width: 128px;
  height: 32px;
  border-radius: 16px;
  background-color: #2c3e50;
}

.curseforge {
  object-fit: cover;
  margin-left: 16px;
}

.stats-banner {
  display: flex;
  margin-left: -10vw;
  margin-right: -10vw;
  width: auto;
  background-color: #d3eeda;
}

.stats-content {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  margin: 0 10%;
  width: 100%;
  padding: 0;
}

.project-section-title {
  font-size: var(--title-font-size);
  font-family: var(--primary-font);
  margin: 0 0 24px;
  padding: 0;
  text-align: center;
}
</style>
