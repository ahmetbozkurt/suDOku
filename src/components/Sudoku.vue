<template>
  <v-data-table :items="levelData" class="elevation-1" hide-actions hide-headers>
    <template slot="items" slot-scope="props">
      <td>
        <v-text-field
          v-bind:id="'A' + props.item.ColNumber"
          v-model="props.item.ColItems.A.value"
          @keypress="isNumber()"
          :maxlength="1"
          :readonly="props.item.ColItems.A.readonly"
          @input="controlValue('A',props.item.ColNumber)"
        ></v-text-field>
      </td>
      <td>
        <v-text-field
          v-bind:id="'B' + props.item.ColNumber"
          v-model="props.item.ColItems.B.value"
          @keypress="isNumber()"
          :maxlength="1"
          :readonly="props.item.ColItems.B.readonly"
          @input="controlValue('B',props.item.ColNumber)"
        ></v-text-field>
      </td>
      <td>
        <v-text-field
          v-bind:id="'C' + props.item.ColNumber"
          v-model="props.item.ColItems.C.value"
          @keypress="isNumber()"
          :maxlength="1"
          :readonly="props.item.ColItems.C.readonly"
          @input="controlValue('C',props.item.ColNumber)"
        ></v-text-field>
      </td>
      <td>
        <v-text-field
          v-bind:id="'D' + props.item.ColNumber"
          v-model="props.item.ColItems.D.value"
          @keypress="isNumber()"
          :maxlength="1"
          :readonly="props.item.ColItems.D.readonly"
          @input="controlValue('D',props.item.ColNumber)"
        ></v-text-field>
      </td>
      <td>
        <v-text-field
          v-bind:id="'E' + props.item.ColNumber"
          v-model="props.item.ColItems.E.value"
          @keypress="isNumber()"
          :maxlength="1"
          :readonly="props.item.ColItems.E.readonly"
          @input="controlValue('E',props.item.ColNumber)"
        ></v-text-field>
      </td>
      <td>
        <v-text-field
          v-bind:id="'F' + props.item.ColNumber"
          v-model="props.item.ColItems.F.value"
          @keypress="isNumber()"
          :maxlength="1"
          :readonly="props.item.ColItems.F.readonly"
          @input="controlValue('F',props.item.ColNumber)"
        ></v-text-field>
      </td>
      <td>
        <v-text-field
          v-bind:id="'G' + props.item.ColNumber"
          v-model="props.item.ColItems.G.value"
          @keypress="isNumber()"
          :maxlength="1"
          :readonly="props.item.ColItems.G.readonly"
          @input="controlValue('G',props.item.ColNumber)"
        ></v-text-field>
      </td>
      <td>
        <v-text-field
          v-bind:id="'H' + props.item.ColNumber"
          v-model="props.item.ColItems.H.value"
          @keypress="isNumber()"
          :maxlength="1"
          :readonly="props.item.ColItems.H.readonly"
          @input="controlValue('H',props.item.ColNumber)"
        ></v-text-field>
      </td>
      <td>
        <v-text-field
          v-bind:id="'I' + props.item.ColNumber"
          v-model="props.item.ColItems.I.value"
          @keypress="isNumber()"
          :maxlength="1"
          :readonly="props.item.ColItems.I.readonly"
          @input="controlValue('I',props.item.ColNumber)"
        ></v-text-field>
      </td>
    </template>
  </v-data-table>
</template>

<style>
td {
  height: 30px;
  width: 30px;
  border: 1px solid;
  text-align: center;
}
td:first-child {
  border-left: solid;
}
td:nth-child(3n) {
  border-right: solid;
}
tr:first-child {
  border-top: solid;
}
tr:nth-child(3n) td {
  border-bottom: solid;
}

table {
  margin: 1em auto;
}

body{
position: fixed;
width: 1024px;
height: 768px;
margin: 2% auto;
left: 0;
right: 0;
}
</style>

<script>
export default {
  data() {
    return {
      mergedId: "",
      elementId: "",
      elementValue: "",
      colitemArray: ["A", "B", "C", "D", "E", "F", "G", "H", "I"],
      errorList:[],
      group1:["A1","A2","A3","B1","B2","B3","C1","C2","C3"],
      group2:["A4","A5","A6","B4","B5","B6","C4","C5","C6"],
      group3:["A7","A8","A9","B7","B8","B9","C7","C8","C9"],
      group4:["D1","D2","D3","E1","E2","E3","F1","F2","F3"],
      group5:["D4","D5","D6","E4","E5","E6","F4","F5","F6"],
      group6:["D7","D8","D9","E7","E8","E9","F7","F8","F9"],
      group7:["G1","G2","G3","H1","H2","H3","I1","I2","I3"],
      group8:["G4","G5","G6","H4","H5","H6","I4","I5","I6"],
      group9:["G7","G8","G9","H7","H8","H9","I7","I8","I9"],

      levelData: [
        {
          ColItems: {
            A: {value:"", readonly:false },
            B: {value:"", readonly:false },
            C: {value:"4", readonly:true },
            D: {value:"", readonly:false },
            E: {value:"", readonly:false },
            F: {value:"", readonly:false },
            G: {value:"8", readonly:true },
            H: {value:"9", readonly:true },
            I: {value:"1", readonly:true },
          },
          ColNumber: "1"
        },
        {
          ColItems: {
            A: {value:"", readonly:false },
            B: {value:"6", readonly:true },
            C: {value:"", readonly:false },
            D: {value:"8", readonly:true },
            E: {value:"", readonly:false },
            F: {value:"", readonly:false },
            G: {value:"", readonly:false },
            H: {value:"3", readonly:true },
            I: {value:"", readonly:false },
          },
          ColNumber: "2"
        },
        {
          ColItems: {
            A: {value:"", readonly:false },
            B: {value:"", readonly:false },
            C: {value:"", readonly:false },
            D: {value:"", readonly:false },
            E: {value:"", readonly:false },
            F: {value:"4", readonly:true },
            G: {value:"", readonly:false },
            H: {value:"6", readonly:true },
            I: {value:"7", readonly:true },
          },
          ColNumber: "3"
        },
        {
          ColItems: {
            A: {value:"", readonly:false },
            B: {value:"", readonly:false },
            C: {value:"", readonly:false },
            D: {value:"6", readonly:true },
            E: {value:"", readonly:false },
            F: {value:"", readonly:false },
            G: {value:"", readonly:false },
            H: {value:"", readonly:false },
            I: {value:"", readonly:false },
          },
          ColNumber: "4"
        },
        {
          ColItems: {
            A: {value:"", readonly:false },
            B: {value:"7", readonly:true },
            C: {value:"8", readonly:true },
            D: {value:"", readonly:false },
            E: {value:"", readonly:false },
            F: {value:"2", readonly:true },
            G: {value:"", readonly:false },
            H: {value:"", readonly:false },
            I: {value:"5", readonly:true },
          },
          ColNumber: "5"
        },
        {
          ColItems: {
            A: {value:"9", readonly:true },
            B: {value:"1", readonly:true },
            C: {value:"2", readonly:true },
            D: {value:"3", readonly:true },
            E: {value:"", readonly:false },
            F: {value:"", readonly:false },
            G: {value:"", readonly:false },
            H: {value:"7", readonly:true },
            I: {value:"8", readonly:true },
          },
          ColNumber: "6"
        },
        {
          ColItems: {
            A: {value:"", readonly:false },
            B: {value:"2", readonly:true },
            C: {value:"3", readonly:true },
            D: {value:"4", readonly:true },
            E: {value:"", readonly:false },
            F: {value:"", readonly:false },
            G: {value:"", readonly:false },
            H: {value:"", readonly:false },
            I: {value:"", readonly:false },
          },
          ColNumber: "7"
        },
        {
          ColItems: {
            A: {value:"", readonly:false },
            B: {value:"", readonly:false },
            C: {value:"", readonly:false },
            D: {value:"", readonly:false },
            E: {value:"", readonly:false },
            F: {value:"9", readonly:true },
            G: {value:"", readonly:false },
            H: {value:"", readonly:false },
            I: {value:"", readonly:false },
          },
          ColNumber: "8"
        },
        {
          ColItems: {
            A: {value:"7", readonly:true },
            B: {value:"", readonly:false },
            C: {value:"9", readonly:true },
            D: {value:"1", readonly:true },
            E: {value:"2", readonly:true },
            F: {value:"", readonly:false },
            G: {value:"", readonly:false },
            H: {value:"", readonly:false },
            I: {value:"6", readonly:true },
          },
          ColNumber: "9"
        }
      ]
    };
  },
  methods: {
    controlValue(colName, colNum) {
      /* eslint-disable */

      //clear input backcolors
      if (!this.checkVertical(colName) || !this.checkHorizontal(colNum) || !this.checkGroup(colName,colNum)) {
        for (let index = 0; index < this.errorList.length; index++) {
          const element = this.errorList[index];
          document.getElementById(element).style.backgroundColor = "#FA8072";
        }
        this.errorList = []
      } else {
      var inputElements = this.getElementByTagName("input")
        for (let index = 0; index < inputElements.length; index++) {
          const element = inputElements[index];
          element.style.backgroundColor = "";
        }
        this.finishControl();
      }
    },
    checkHorizontal(
      colNum //yatay
    ) {
      let pointer = 0;
      let stopProcess = false;
      for (let index = 0; index < this.levelData.length; index++) {
        if (this.levelData[index].ColNumber == colNum) {
          const element = this.levelData[index].ColItems;
          for (
            let itemArrayIndex = 0;
            itemArrayIndex < this.colitemArray.length;
            itemArrayIndex++
          ) {
            pointer = itemArrayIndex;
            const item = element[this.colitemArray[itemArrayIndex]].value;
          if (item != '') {
              for (
                let subIndex = 0;
                subIndex < this.colitemArray.length;
                subIndex++
              ) {
                if (pointer != subIndex) {
                  const subItem = element[this.colitemArray[subIndex]].value;
                  if (item == subItem) {
                    this.errorList.push(this.colitemArray[pointer]  +colNum)
                    this.errorList.push(this.colitemArray[subIndex] +colNum)
                    console.log(
                      this.colitemArray[pointer] +
                        colNum +
                        "-" +
                        this.colitemArray[subIndex] +
                        colNum +
                        " değerleri aynı"
                    );
                    return false;
                  }
                }
              }
            }
          }
          break;
        }
      }
      return true;
    },
    checkVertical(
      colName,
      value //dikey
    ) {
      let pointer = 0;
      let stopProcess = false;
      for (let index = 0; index < this.levelData.length; index++) {
        pointer = index;
        const element = this.levelData[index].ColItems[colName].value;
        if (element != '') {
          for (let subIndex = 0; subIndex < this.levelData.length; subIndex++) {
            if (pointer != subIndex) {
              const subElement = this.levelData[subIndex].ColItems[colName].value;
              if (element == subElement) {

                this.errorList.push(colName +(pointer + 1))
                this.errorList.push(colName +(subIndex + 1))

                console.log(
                  colName +
                    (pointer + 1) +
                    "-" +
                    colName +
                    (subIndex + 1) +
                    " değerleri aynı"
                );
                return false;
              }
            }
          } 
        }
      }
      return true;
    },
    checkGroup(colName,colNum) {
      let groupArray = this.findGroup(colName,colNum)
      let groupValues = []
      let pointer = 0;
      for (let index = 0; index < groupArray.length; index++) {
        const element = groupArray[index];
        var item = {value:this.getElementByIdForValue(element),id:element}
        groupValues.push(item);
      }
      for (let index = 0; index < groupValues.length; index++) {
        const item = groupValues[index].value;
        pointer = index;
        if (item != '') {
            for (let subIndex = 0; subIndex < groupValues.length; subIndex++) {
            if (pointer != subIndex) {
                const subItem = groupValues[subIndex].value;
                  if (item == subItem) {
                    this.errorList.push(groupValues[index].id)
                    this.errorList.push(groupValues[subIndex].id)
                    console.log(groupValues[index].id +"-" +groupValues[subIndex].id +" değerleri aynı");
                    return false;
              }
            }
          }
        }
      }
      return true;
    },
    getElementById(id) {
      return document.getElementById(id).value;
    },
    finishControl()
    {
      let sum = 0;
      var inputElements = this.getElementByTagName("input")
      for (let index = 0; index < inputElements.length; index++) {
        const element = inputElements[index];
        if (element.value == "") {
          break;
        }
        else{
          sum = parseInt(sum) + parseInt(element.value);
        }      
      }
      if (sum == 405) {
        var inputElements = this.getElementByTagName("input")
        for (let index = 0; index < inputElements.length; index++) {
          const element = inputElements[index];
          element.style.backgroundColor = "#00944D";
        }
      }
    },
    getElementByTagName(tag) {
      return document.getElementsByTagName(tag);
    },
    getElementByIdForValue(id) {
      return document.getElementById(id).value;
    },
    isNumber: function(evt) {
      evt = (evt) ? evt : window.event;
      var charCode = (evt.which) ? evt.which : evt.keyCode;
      if (evt.keyCode != 48) {
        if ((charCode > 31 && (charCode < 48 || charCode > 57)) && charCode !== 46) {
          evt.preventDefault();
        } 
        else { return true;}
      }
      else
      {
          evt.preventDefault();
      }
    },
    findGroup(colName,colNum)
    {
      if(colNum == 1 || colNum == 2 || colNum == 3)
      {
        if(colName == "A" || colName == "B" || colName == "C")
        {
            return this.group1
        }
        if(colName == "D" || colName == "E" || colName == "F")
        {
            return this.group4
        }
        if(colName == "G" || colName == "H" || colName == "I")
        {
            return this.group7
        }
      }
      if(colNum == 4 || colNum == 5 || colNum == 6)
      {
        if(colName == "A" || colName == "B" || colName == "C")
        {
            return this.group2
        }
        if(colName == "D" || colName == "E" || colName == "F")
        {
            return this.group5
        }
        if(colName == "G" || colName == "H" || colName == "I")
        {
            return this.group8
        }
      }
      if(colNum == 7 || colNum == 8 || colNum == 9)
      {
        if(colName == "A" || colName == "B" || colName == "C")
        {
            return this.group3
        }
        if(colName == "D" || colName == "E" || colName == "F")
        {
            return this.group6
        }
        if(colName == "G" || colName == "H" || colName == "I")
        {
            return this.group9
        }
      }
        return this.group1
    }
  }
};
</script>