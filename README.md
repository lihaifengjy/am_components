# am_components
am_components

# am-table
    目前集成了普通分页表格和增强表格的功能
    引用形式：<am-table-v></am-table-v>
    类型：
        普通分页表格:
            参数：必填：url，pagetype:'page-table',headers(类型展示选择text，自定义插槽选择custom),选填：params,pager
            例子：<am-table-v pagetype="page-table" headers="headers" :params="" queryurl="/xxx/x/"></am-table-v>
        增强表格:
            参数：pagetype:'power-table',headers,data
            例子：<am-table-v pagetype="power-table" headers="headers" :data.sync="data" ::cfg=""></am-table-v>
    ##pagetype:'page-table','power-table'
    ##headers:{
        type: 系统：selection/index/expand 自定义：checkbox,date,input,custom,select,radio,textarea,number,text
        label: 
        prop: 
        width: 
        fixed:  true, left, right
        align: left/center/right
        disabled: ,
        sortable: true, false, 'custom',
        header-align: left/center/right
        formatter: function,
        custom: slot的name <template v-slot:custom的值>xxx</template>
    }
    ##queryurl: ''
    ##params:{

    }
    ##cfg: {
        newRow: true,
        deleteRow: true,
        pageable:true,
        pagesize: 5,
    },
    ##pager: {
        pageSize: 10,
        total: 0,
        current: 1
    },