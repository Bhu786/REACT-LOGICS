# REACT-LOGICS


##MULTIPLE BUTTON ME LOGIC 
```react.jsx
import {React,useState} from 'react';
import './CollegeAllCourses.css'
import { Link, useNavigate } from "react-router-dom"
import Table2 from '../../Filter/FilterCollege';
import Table3 from '../../Filter/FilterCompExam';
import Table1 from '../../Filter/FilterSchool';


const CollegeAllCourses = () => {

 
  const [selectedTable, setSelectedTable] = useState(null);

  // Functions to handle button clicks
  const showTable1 = () => setSelectedTable(1);
  const showTable2 = () => setSelectedTable(2);
  const showTable3 = () => setSelectedTable(3);

  return (
    <>
        
        <div id="college-all-course-inner-main-wrapper">

        <div className="course-header-with-btns-table-page">
          <h5>All Notes</h5>

          
        </div>

        <div id="powered-by-app-mingle-media-mains">

         <div className='main-button'>
         <button onClick={showTable1}>School</button>
         <button onClick={showTable2}>College</button>
         <button onClick={showTable3}>Competitive Exam</button>
         </div>
          
      </div>
 <div>
      {selectedTable === 1 && (
        <div>
          <Table1 />
        </div>
      )}

      {selectedTable === 2 && (
        <div>
          <Table2 />
        </div>
      )}

      {selectedTable === 3 && (
        <div>
          <Table3 />
        </div>
      )}
    </div>
        
        </div>

    </>
  );
}

export default CollegeAllCourses;
```


##
