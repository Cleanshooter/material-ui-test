## This is a complete copy and frezee of MUI 0.18.1

### Install

`npm i -S https://github.com/Cleanshooter/material-ui-test.git`

### Differences
 * Table body has the ability to setSelectedRows programatically

Conceptual Example (not fully funtional):
```javascript
import React, { Component } from 'react';
import PropTypes from 'prop-types';

// Material UI Components
import {
  Table,
  TableHeader,
  TableHeaderColumn,
  TableRow,
  TableRowColumn
} from 'material-ui/Table';
import { TableBody } from 'material-ui-test/Table';

class Analyses extends Component {
  constructor() {
    super();
    this.state = {
      selected: ''
    };
  }

  render() {

    const rowSelected = (selection) => {
      this.setState({selected: selection});
    };
    
    const someEvent = () => {
      this.setState({
        selected: []
      });
    };
    
    const rows = analyses.map((data, index) => {
      //fancy row stuff
    });

    return (
      <div>
        <Table
          multiSelectable
          onRowSelection={rowSelected}
        >
          <TableHeader>
            <TableRow>
              <TableHeaderColumn >Details</TableHeaderColumn>
              <TableHeaderColumn >Message</TableHeaderColumn>
              <TableHeaderColumn >Stuff</TableHeaderColumn>
              <TableHeaderColumn >Date</TableHeaderColumn>
            </TableRow>
          </TableHeader>
          <TableBody
            showRowHover
            stripedRows
            deselectOnClickaway={false}
            setSelectedRows={this.state.selected}
          >
            {rows}
          </TableBody>
        </Table>
      </div>
    );
  }
}
```
** Warning I'll only be updating this once in a while when I update my project dependencies... **
