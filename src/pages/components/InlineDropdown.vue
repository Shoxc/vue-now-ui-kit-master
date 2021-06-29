<template>
<div>
    <div class="control-section">
        <div id='content' style="margin: 0px auto; width:350px; padding-top: 40px;">
            <span id="contentText">React top expert of this week is
            <ejs-dropdownlist id='employee' :dataSource='data' :fields='fields' :popupHeight='height' :width='width' cssClass='ddl-inlinecss' :value='value' :popupWidth='popupWidth' :placeholder='watermark'>
            </ejs-dropdownlist>
            </span>
        </div>
    </div>
</div>
</template>
<style>

    .ddl-inlinecss.e-ddl .e-input-group-icon.e-ddl-icon {
        display: none;
    }

    .ddl-inlinecss.e-ddl .e-control.e-dropdownlist.e-input {
        font-size: 17px;
        font-weight: 500;
        margin: -5px 0px 0px 0px;
        padding: 0px;
    }

    .material .ddl-inlinecss.e-ddl .e-control.e-dropdownlist.e-input {
        margin: 4px 0px 0px 0px;
    }

    .bootstrap .ddl-inlinecss.e-ddl .e-control.e-dropdownlist.e-input {
        margin-top: -1px;
    }

    .ddl-inlinecss.e-input-group.e-control-wrapper.e-ddl::before,
    .ddl-inlinecss.e-input-group.e-control-wrapper.e-ddl::after {
        content: none;
    }

    .ddl-inlinecss.e-input-group.e-control-wrapper.e-ddl,
    .ddl-inlinecss.e-input-group.e-control-wrapper.e-ddl:hover,
    .ddl-inlinecss.e-input-group.e-ddl.e-input-focus,
    .ddl-inlinecss.e-input-group.e-ddl.e-input-focus::before,
    .ddl-inlinecss.e-input-group.e-ddl.e-input-focus::after {
        border-width: 0px;
        border: none;
        border-bottom: 1px dashed black;
        box-shadow: none;
    }
</style>
<script>
import Vue from "vue";
import { MultiSelectPlugin } from "@syncfusion/ej2-vue-dropdowns";
import { Query } from '@syncfusion/ej2-data';
import * as data from './dataSource.json';

Vue.use(MultiSelectPlugin);

export default Vue.extend ({
    data: function() {
        return {
            fields: { text: 'Name'},
            height: '220px',
            width: '63px',
            popupWidth: '140px',
            value: 'Michael',
            watermark: 'Select an employee',
            data: data['employees'],
        };
    }
});
</script>

