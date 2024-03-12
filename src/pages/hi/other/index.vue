<script setup lang="ts">
</script>

<template>
  <NCard
    title="card"
    :bordered="false"
  >
    <template #header-extra>
      <NButton type="primary">
        {{ 'test' }}
      </NButton>
    </template>
    <NTabs
      type="line"
      animated
    >
      <NTabPane
        name="config"
        tab="tab1"
      >
        <NGrid :x-gap="12" mt-4>
          <NGridItem span="4">
            <NSelect
              :consistent-menu-width="false"
            />
          </NGridItem>
          <NGridItem span="8">
            <NInput
              text-left
            />
          </NGridItem>
          <NGridItem span="4">
            <NButton attr-type="button">
              {{ 'BBB' }}
            </NButton>
          </NGridItem>
        </NGrid>
        <NGrid :x-gap="12" mt-4>
          <NGridItem span="8">
            <NUpload
              :max="1"
              accept=".xlsx"
              :multiple="false"
              text-left
            >
              <NButton>
                {{ 'select' }}
              </NButton>
            </NUpload>
          </NGridItem>
          <NGridItem span="4">
            <NButton secondary round type="primary">
              <template #icon>
                <n-icon i-carbon-cloud-download />
              </template>
              {{ 'download' }}
            </NButton>
          </NGridItem>
        </NGrid>
      </NTabPane>
      <NTabPane
        name="preview"
        tab="tabB"
      >
        <NDataTable
          :default-expand-all="true"
        />
      </NTabPane>
    </NTabs>
  </NCard>
</template>

<route lang="yaml">
  meta:
    layout: default
    name: hiIndex
  </route>
