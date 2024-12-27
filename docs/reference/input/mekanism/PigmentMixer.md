---
telem:
  adapter:
    id: 'pigmentMixer'
    name: 'Pigment Mixer'
    categories: '{ "basic", "advanced", "input", "output", "energy" }'
---

<script setup>
  import { data as metrics } from './common/metrics.data.ts'
</script>

# Mekanism Pigment Mixer Input <RepoLink path="lib/input/mekanism/PigmentMixerInputAdapter.lua" />

<!--@include: ./common/preamble.md -->

### Basic

<MetricTable
  prefix="mekpigmentmixer:"
  :metrics="[
    { name: 'input_left_item_count',          value: '0 - inf',   unit: 'item'  },
    { name: 'input_right_item_count',         value: '0 - inf',   unit: 'item'  },
    { name: 'input_left_filled_percentage',   value: '0.0 - 1.0'                },
    { name: 'input_right_filled_percentage',  value: '0.0 - 1.0'                },
    { name: 'output_item_count',              value: '0 - inf',   unit: 'item'  },
    { name: 'output_filled_percentage',       value: '0.0 - 1.0'                },
    { name: 'energy_usage',                   value: '0.0 - inf', unit: 'FE/t'  },
    ...metrics.genericMachine.basic
  ]"
/>

### Advanced

<MetricTable
  prefix="mekpigmentmixer:"
  :metrics="[
    ...metrics.genericMachine.advanced
  ]"
/>

### Input

<MetricTable
  prefix="mekpigmentmixer:"
  :metrics="[
    { name: 'input_left',           value: '0.0 - inf', unit: 'B' },
    { name: 'input_left_capacity',  value: '0.0 - inf', unit: 'B' },
    { name: 'input_left_needed',    value: '0.0 - inf', unit: 'B' },
    { name: 'input_right',          value: '0.0 - inf', unit: 'B' },
    { name: 'input_right_capacity', value: '0.0 - inf', unit: 'B' },
    { name: 'input_right_needed',   value: '0.0 - inf', unit: 'B' }
  ]"
/>

### Output

<MetricTable
  prefix="mekpigmentmixer:"
  :metrics="[
    { name: 'output',           value: '0.0 - inf', unit: 'B' },
    { name: 'output_capacity',  value: '0.0 - inf', unit: 'B' },
    { name: 'output_needed',    value: '0.0 - inf', unit: 'B' }
  ]"
/>

### Energy

<MetricTable
  prefix="mekpigmentmixer:"
  :metrics="[
    ...metrics.genericMachine.energy
  ]"
/>