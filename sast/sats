#!/bin/bash
# Pipeline DevSecOps - Análise de Segurança com Trivy

echo "Iniciando análise de segurança do container com Trivy..."
docker pull your-image:latest

if trivy image --severity HIGH,CRITICAL your-image:latest; then
    echo "Nenhuma vulnerabilidade crítica encontrada. Prosseguindo com o deploy..."
else
    echo "Vulnerabilidades críticas detectadas. O deploy foi interrompido."
    exit 1
fi