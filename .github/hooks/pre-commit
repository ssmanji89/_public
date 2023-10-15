#!/bin/sh

# Navigate to _posts directory
cd _posts || exit 1

# Iterate through each Markdown file
for file in /_posts/*.md; do
  # Check if date exists in front matter
  if ! grep -q "^date:" "$file"; then
    # Extract filename without extension
    filename=$(basename -- "$file")
    name_without_extension="${filename%.*}"
    
    # Add date and filename to front matter
    sed -i "1 a\date: $(date +'%Y-%m-%d %H:%M:%S %z')_$name_without_extension" "$file"
  fi
done
