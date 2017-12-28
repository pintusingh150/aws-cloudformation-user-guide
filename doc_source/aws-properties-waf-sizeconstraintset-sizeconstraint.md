# AWS WAF SizeConstraintSet SizeConstraint<a name="aws-properties-waf-sizeconstraintset-sizeconstraint"></a>

`SizeConstraint` is a property of the [AWS::WAF::SizeConstraintSet](aws-resource-waf-sizeconstraintset.md) resource that specifies a size constraint and which part of a web request that you want AWS WAF to constrain\.

## Syntax<a name="w3ab2c21c14e1645b5"></a>

### JSON<a name="aws-properties-waf-sizeconstraintset-sizeconstraint-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-waf-sizeconstraintset-sizeconstraint-comparisonoperator)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-waf-sizeconstraintset-sizeconstraint-fieldtomatch)" : Field to match,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-waf-sizeconstraintset-sizeconstraint-size)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-waf-sizeconstraintset-sizeconstraint-texttransformation)" : String
}
```

### YAML<a name="aws-properties-waf-sizeconstraintset-sizeconstraint-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-waf-sizeconstraintset-sizeconstraint-comparisonoperator): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-waf-sizeconstraintset-sizeconstraint-fieldtomatch):
  Field to match
[[ERROR] BAD/MISSING LINK TEXT](#cfn-waf-sizeconstraintset-sizeconstraint-size): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-waf-sizeconstraintset-sizeconstraint-texttransformation): String
```

## Properties<a name="w3ab2c21c14e1645b7"></a>

`ComparisonOperator`  
The type of comparison that you want AWS WAF to perform\. AWS WAF uses this value in combination with the `Size` and `FieldToMatch` property values to check if the size constraint is a match\. For more information and valid values, see the `ComparisonOperator` content for the [SizeConstraint](http://docs.aws.amazon.com/waf/latest/APIReference/API_SizeConstraint.html) data type in the *AWS WAF API Reference*\.  
*Required: *Yes  
*Type*: String

`FieldToMatch`  
The part of a web request that you want AWS WAF to search, such as a specific header or a query string\.  
*Required: *Yes  
*Type*: [AWS WAF SizeConstraintSet SizeConstraint FieldToMatch](aws-properties-waf-sizeconstraintset-sizeconstraint-fieldtomatch.md)

`Size`  
The size in bytes that you want AWS WAF to compare against the size of the specified `FieldToMatch`\. AWS WAF uses `Size` in combination with the `ComparisonOperator` and `FieldToMatch` property values to check if the size constraint of a web request is a match\. For more information and valid values, see the `Size` content for the [SizeConstraint](http://docs.aws.amazon.com/waf/latest/APIReference/API_SizeConstraint.html) data type in the *AWS WAF API Reference*\.  
*Required: *Yes  
*Type*: Integer

`TextTransformation`  
Specifies how AWS WAF processes the `FieldToMatch` property before inspecting a request for a match\. Text transformations eliminate some of the unusual formatting that attackers use in web requests in an effort to bypass AWS WAF\. If you specify a transformation, AWS WAF transforms the `FieldToMatch` before inspecting a web request for a match\.  
For example, AWS WAF can replace white space characters \(such as `\t` and `\n`\) with a single space\. For valid values, see the `TextTransformation` content for the [SizeConstraint](http://docs.aws.amazon.com/waf/latest/APIReference/API_SizeConstraint.html) data type in the *AWS WAF API Reference*\.  
*Required: *Yes  
*Type*: String