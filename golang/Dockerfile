FROM golang:alpine

ENV GOPROXY "https://goproxy.cn,direct"
ENV GO111MODULE on

# 项目工作目录
WORKDIR $APP_CODE_CONTAINER_PATH/goblog

#ADD go.mod $APP_CODE_CONTAINER_PATH/goblog
#ADD go.sum $APP_CODE_CONTAINER_PATH/goblog
# 初始化目录
RUN go mod init goblog
# 同步依赖包，添加需要的，移除多余的
RUN go mod tidy
# 下载依赖
RUN go mod download
#
RUN go mod vendor
# 清理缓存
RUN go clean -modcache

EXPOSE 8000