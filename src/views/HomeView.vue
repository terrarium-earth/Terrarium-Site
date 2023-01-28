<template>
  <div class="home">
    <div class="home-header">
      <p class="home-title">Terrarium</p>
      <p class="home-subtitle">Creating new and exciting Minecraft content!</p>
      <p class="home-text">
        We are a community of Minecraft mod developers and content creators
        dedicated to creating a better Minecraft experience for everyone. We're
        working on a variety of the communities favorite mods, including
        Chipped, Spirit & Ad Astra!
      </p>
      <div class="downloads">
        <a href="https://www.curseforge.com/members/terrariumearth/projects">
          <img
            alt="modrinth"
            class="platform"
            src="https://raw.githubusercontent.com/modrinth/art/a05e2307b42762d64a370a3cf3e8b6b30735dce1/Branding/Wordmark/wordmark-dark.svg"
          />
        </a>
        <a href="https://modrinth.com/user/Terrarium">
          <img
            alt="curseforge"
            class="platform curseforge"
            src="https://www.userlogos.org/files/curseforge.png"
          />
        </a>
      </div>
    </div>
    <img src="@/assets/home.png" />
  </div>
</template>

<style>
/* put content into rows */
.home {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  margin: 0;
  background-color: #bae5c5;
}

.home-header {
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin: 0;
  width: min-content;
}

.home-title {
  font-size: 128px;
  font-family: Fredoka One;
  margin: 0;
  padding: 0;
  margin-bottom: 24px;
}

.home-subtitle {
  font-size: 24px;
  font-family: Poppins;
  text-align: justify;
  margin: 0;
  color: #4a7263;
  font-weight: bold;
}

.home-text {
  font-size: 16px;
  font-family: Poppins;
  text-align: justify;
  margin: 0;
  color: #4b4b4b;
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
</style>
