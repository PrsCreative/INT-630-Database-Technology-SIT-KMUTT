# INT-630-Database-Technology-SIT-KMUTT


# NppExc
  > "C:\INT630\AltovaXML.exe" /oi /xq "$(FULL_CURRENT_PATH)
  > 

## Well Form Check
  
  
# AltovaXML Command line


## Query From My projects.xml

    doc("projects.xml")/*
    doc("projects.xml")/child::projectList
    doc("projects.xml")/child::node()
    doc("projects.xml")/child::comment()
    doc("projects.xml")/child::element()
    doc("projects.xml")/child::element(projectList)
  
## Comment
    (:              :)

## For let XQuery
    for $node in doc("projects.xml")/child::node()
    return $node

    for $node at $count in doc("projects.xml")/child::node()
    return <result number='{$count}'>{$node}</result>

  ## Find data in XML File
    ## find num of project allther project
    for $node at $count in doc("projects.xml")/projectList/project/attribute::num/string() 
    return <result number='{$count}'>{$node}</result>
    
    ## find title of project
    for $node at $count in doc("projects.xml")/projectList/project/title
    return <result number='{$count}'>{$node}</result>
    
    ## find review of proejct from XML
    for $node at $count in doc("projects.xml")/projectList/project/attribute::num/string()
    return <result number='{$count}'>{$node}</result>



## Link
https://www.w3.org/TR/xpath-functions-30/
