<template>
  <q-page>
    <div class="q-py-lg q-px-md row items-end q-col-gutter-md">
      <div class="col">

        <q-input bottom-slots v-model="newContent"
                 placeholder="Whats Happening"
                 counter maxlength="280"
                 autogrow
                 class="new-queet">
          <template v-slot:before>
            <q-avatar size="xl">
              <img src="https://secure.gravatar.com/avatar/78f80907703dd679a6bba66bf10d83b5">
            </q-avatar>

          </template>
        </q-input>
      </div>
      <div class="col col-shrink">
        <q-btn unelevated rounded color="primary"
               class="q-mb-lg "
               label="Qweet" no-caps
               :disable="!newContent"/>
      </div>

    </div>
    <q-separator size="10px"
                 color="grey-2"
                 class="divider"
    />

    <q-list>

      <q-item class="q-py-md">
        <q-item-section avatar>
          <q-avatar size="xl">
            <img src="https://secure.gravatar.com/avatar/78f80907703dd679a6bba66bf10d83b5">
          </q-avatar>
        </q-item-section>

        <q-item-section>
          <q-item-label><strong>Alfred Anyan</strong>
          <span class="text-grey-7">@alfredanyan</span>
          </q-item-label>
          <q-item-label>
            <span class="text-weight-bold">Janet</span>
            -- I'll be in your neighborhood doing errands this
            weekend. Do you want to grab brunch?
          </q-item-label>
        </q-item-section>

        <q-item-section side top>
          1 min ago
        </q-item-section>
      </q-item>

    </q-list>
  </q-page>
</template>

<script>
import {defineComponent} from 'vue';

export default defineComponent({
  name: 'PageHome',
  data() {
    return {
      newContent: ''
    }
  }
})

</script>

<style lang="sass">
.new-queet
  textarea
    font-size: 19px
    line-height: 1.4 !important

.divider
  border-top: 1px solid
  border-bottom: 1px solid
  border-color: $grey-4
</style>
