<template>
  <div class="container-fluid">
    <div class="wrapper-asus-translate-textarea">
      <div class="row">
        <div class="col-width-49percent mr-0-4 border border-dark min-height-268px">
          <div class="lang-select">
            <div class="source-language">
              <p class="text-capitalize h4">english</p>
            </div>
            <div class="btn-switch">
              <svg
                id="Layer"
                enable-background="new 0 0 64 64"
                height="24"
                viewBox="0 0 64 64"
                width="24"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="m10 26h39.172l-3.586 3.586c-.781.781-.781 2.047 0 2.828.391.391.902.586 1.414.586s1.023-.195 1.414-.586l7-7c.781-.781.781-2.047 0-2.828l-7-7c-.781-.781-2.047-.781-2.828 0s-.781 2.047 0 2.828l3.586 3.586h-39.172c-1.104 0-2 .896-2 2s.896 2 2 2z"
                />
                <path
                  d="m54 38h-39.172l3.586-3.586c.781-.781.781-2.047 0-2.828-.78-.781-2.048-.781-2.828 0l-7 7c-.781.781-.781 2.047 0 2.828l7 7c.39.391.902.586 1.414.586s1.024-.195 1.414-.586c.781-.781.781-2.047 0-2.828l-3.586-3.586h39.172c1.104 0 2-.896 2-2s-.896-2-2-2z"
                />
              </svg>
            </div>
          </div>
          <div id="sourceEditArea" class="source-edit" style="display:block;" tabindex="-1">
            <label for="txtSource" class="width-label">
              <textarea
                placeholder="Type the text to translate."
                id="txtSource"
                name="txtSource"
                class="edit_box"
                rows="1"
                style="resize: inherit; min-height: 38px;"
                tabindex="-1"
              ></textarea>
            </label>
          </div>
          <p class="text_count">0 / 5000</p>
        </div>
        <div class="col-width-49percent mr-0-4 border border-dark min-height-268px"></div>
      </div>
    </div>
  </div>
</template>
<style>
.wrapper-asus-translate-textarea {
  padding: 32px;
}

.col-width-49percent {
  width: 49%;
}

.mr-0-4 {
  margin: 0 4px;
}

.min-height-268px {
  min-height: 268px;
}

.lang-select {
  border-bottom: 1px solid rgba(0, 0, 0, 0.05);
  margin-left: 1px;
  height: 35px;
}

.source-language {
  float: left;
  border-right: 0.5px solid #00008b;
  position: relative;
  margin-right: 82%;
}

.btn-switch {
  position: relative;
  top: 0;
  right: 0;
}

.source-edit {
  min-height: 135px;
  padding: 28px 20px 63px;
  position: relative;
  height: auto;
}

.edit_box {
  font-size: 30px;
  line-height: 1.26em;
  backface-visibility: hidden;
  background-color: transparent;
  border: 0;
  color: #999;
  overflow: hidden;
  transform: translateZ(0);
  display: inline-block;
  width: 100%;
  word-break: break-word;
  min-height: 39px;
  height: auto;
}

.width-label {
  width: 100%;
}

.text_count {
  position: relative;
  left: 89%;
  color: #bbb;
  font-size: 18px;
  line-height: 19px;
  display: inline-block;
}
</style>
<script>
$("#txtSource")
  .on("change keyup keydown paste cut", "textarea", function () {
    $(this).height(0).height(this.scrollHeight);
  })
  .find("textarea")
  .change();
</script>