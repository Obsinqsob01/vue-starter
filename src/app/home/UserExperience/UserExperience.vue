<template>
  <div :class="[$style.userExperience, 'featureSection']">
    <vue-grid>
      <vue-grid-row>
        <vue-grid-item fill class="vueGridItem">
          <h2>User experience</h2>
        </vue-grid-item>

        <vue-grid-item class="vueGridItem">
          <vue-panel class="vuePanel">
            <vue-panel-body>
              <vue-icon-spinner />
              <h3>Animations</h3>
              <p>A stable animations set up already included (<a href="http://animejs.com/" target="_blank"
                                                                 rel="noopener">anime.js</a>).</p>
            </vue-panel-body>
          </vue-panel>
        </vue-grid-item>

        <vue-grid-item class="vueGridItem">
          <vue-panel class="vuePanel">
            <vue-panel-body>
              <vue-icon-mobile />
              <h3>Progressive-Web-App</h3>
              <p>Offline-first support with service-workers and a lighthouse score as high as possible (90+).</p>
            </vue-panel-body>
          </vue-panel>
        </vue-grid-item>

        <vue-grid-item class="vueGridItem">
          <vue-panel class="vuePanel">
            <vue-panel-body>
              <vue-icon-puzzle-piece />
              <h3>Components</h3>
              <p>
                A flexible component library that'll be extended over time.
              </p>
              <p>
                Visit the
                <router-link to="/components">Component's page</router-link>
                to see a preview of the available components.
              </p>
            </vue-panel-body>
          </vue-panel>
        </vue-grid-item>
      </vue-grid-row>
    </vue-grid>
  </div>
</template>

<script lang="ts">
  import VueGrid            from '../../shared/components/VueGrid/VueGrid.vue';
  import VueGridItem        from '../../shared/components/VueGridItem/VueGridItem.vue';
  import VuePanel           from '../../shared/components/VuePanel/VuePanel.vue';
  import VuePanelBody       from '../../shared/components/VuePanel/VuePanelBody/VuePanelBody.vue';
  import VueGridRow         from '../../shared/components/VueGridRow/VueGridRow.vue';
  import VueIconSpinner     from '../../shared/components/icons/VueIconSpinner/VueIconSpinner.vue';
  import VueIconMobile      from '../../shared/components/icons/VueIconMobile/VueIconMobile.vue';
  import VueIconPuzzlePiece from '../../shared/components/icons/VueIconPuzzlePiece/VueIconPuzzlePiece.vue';

  export default {
    components: {
      VueIconPuzzlePiece,
      VueIconMobile,
      VueIconSpinner,
      VueGrid,
      VueGridItem,
      VuePanel,
      VuePanelBody,
      VueGridRow,
    },
  };
</script>

<style lang="scss" module>
  @import "../../shared/styles";

  .userExperience {
    display:    block;
    text-align: center;

    i {
      display:    inline-block;
      height:     $font-size-h1;
      width:      $font-size-h1;
      margin-top: $space-unit;
    }

  }
</style>
