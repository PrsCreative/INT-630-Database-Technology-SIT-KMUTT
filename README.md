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
  
## Comment XQuery
    (:              :)

## For let XQuery
    for $node in doc("projects.xml")/child::node()
    return $node

    for $node at $count in doc("projects.xml")/child::node()
    return <result number='{$count}'>{$node}</result>

  ## Find data in XML File
    
    ## find num of project allther project
    ## แบบย่อ
    for $node at $count in 
    doc("projects.xml")/projectList/project/attribute::num/string() 
    return <result number='{$count}'>{$node}</result>

    ## แบบเต็ม
    for $node at $count in 
    doc("projects.xml")/child::projectList/child::project/attribute::num/string() 
    return <result number='{$count}'>{$node}</result>
    ------------------------------------------------------------------------------------------------------

    ## find title of project
    ## แบบย่อ
    for $node at $count in 
    doc("projects.xml")/projectList/project/title
    return <result number='{$count}'>{$node}</result>

    ## แบบเต็ม
    for $node at $count in 
    doc("projects.xml")/child::projectList/child::project/title
    return <result number='{$count}'>{$node}</result>
    ------------------------------------------------------------------------------------------------------
    
    ## find review of proejct from XML
    ## แบบย่อ
    for $node at $count in 
    doc("projects.xml")/projectList/project/attribute::num/string()
    return <result number='{$count}'>{$node}</result>

    ## แบบเต็ม
    for $node at $count in 
    doc("projects.xml")/child::projectList/child::project/attribute::num/string()
    return <result number='{$count}'>{$node}</result>
    ------------------------------------------------------------------------------------------------------

  ## Predicate
  
    # Union
    for $node at $count in 
    doc("projects.xml")/projectList/project[advisor[fn='Jack'] union advisor[ln='Bryan']]/title/text()return <result number='{$count}'>{$node}</result>
## Link
https://www.w3.org/TR/xpath-functions-30/
