<template>
  <vgl-renderer>
    <vgl-defs>
      <template #tetrahedron>
        <vgl-tetrahedron-geometry />
      </template>
    </vgl-defs>
    <template #scene>
      <vgl-scene>
        <vgl-mesh>
          <template #geometry>
            <vgl-use href="tetrahedron" />
          </template>
          <template #material>
            <vgl-mesh-standard-material/>
          </template>
        </vgl-mesh>
        <vgl-directional-light
          :position-x="2"
          :position-y="1.5"
          :position-z="1"
        />
      </vgl-scene>
    </template>
    <template #camera>
      <vgl-perspective-camera
        :position-x="5"
        :position-y="1.5"
        :position-z="1.5"
        rotation="lookAt"
      />
    </template>
  </vgl-renderer>
</template>

<script>
import { VglRenderer, VglDefs, VglUse, VglScene, VglTetrahedronGeometry, VglMeshStandardMaterial, VglDirectionalLight, VglMesh, VglPerspectiveCamera, } from 'vue-gl';

export default {
  components: {
    VglRenderer,
    VglDefs,
    VglUse,
    VglScene,
    VglTetrahedronGeometry,
    VglMeshStandardMaterial,
    VglDirectionalLight,
    VglMesh,
    VglPerspectiveCamera,
  },
};
</script>